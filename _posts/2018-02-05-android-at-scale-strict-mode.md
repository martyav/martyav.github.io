---
layout: post
title: "Android@Scale: Eliminating Long Tail Jank With Strict Mode"
---

The second-to-last session at last week's [Android@Scale](https://atscaleconference.com/events/android-scale-2018/) conference was a talk by [Kurt Nelson](https://plus.google.com/+KurtNelson), of [Big Nerd Ranch](https://www.bignerdranch.com/about/the-team/kurt-nelson/) and Google. He gave a [similar talk](https://droidcon-server.herokuapp.com/showSession/103034) at [DroidCon](http://droidcon.nyc/) last year, so if you missed out, you're in luck. My notes on this session, concerning Strict Mode, aren't as extensive as my last post about [Android@Scale and React Native](https://martyav.github.io/2018-02-01-notes-on-React-Native/), but they do provide a primer on what [Strict Mode](https://developer.android.com/reference/android/os/StrictMode.html) is and why you should consider using it.

Google defines Strict Mode as "a developer tool which detects things you might be doing by accident". When you turn it on, you get extensive warnings about issues that can slow the app down or make it feel unresponsive. These are problems you might not ever notice otherwise when you are testing. 

While you, as a developer, may be using top technology as a matter of pride, many Android users in the rest of the world own older phones with low-quality parts. It's what they can afford. However, when you test your app on a top-of-the-line phone, and someone using an end-of-the-line phone downloads it, they may encounter dropped frames and memory leaks that slow the app to a crawl. You, on your expensive phone, never noticed these problems because you had the horsepower to charge over these issues. Less powerful phones are more sensitive to these problems — and then you get an irritated userbase.

Strict Mode can detect slow calls, resource mismatches, expensive unbuffered IO operations, network calls that wind up on the main thread, and read/write operations, which have particularly unpredictable timing. Strict Mode can also detect [virtual machine leaks](https://www.toptal.com/java/hunting-memory-leaks-in-java), though you can also use the open source library [Leak Canary](https://github.com/square/leakcanary).

You can turn on Strict Mode by calling a builder in your app's onCreate(). Make sure you turn this off in any user builds — having Strict Mode silently run can make things slightly slower.

If you start up Strict Mode and encounter some warnings, here are some common fixes:

## Slow calls
Slow calls can often be put on the background thread so they are no longer blocking the UI thread and causing dropped frames. A frame rate of 60fps gives you only 16ms for each task on the main thread to complete. If the call can't complete it in that amount of time, it needs to go. Using [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask.html), [dependency injection](https://tech.just-eat.com/2015/10/26/dependency-injection-on-android/), or [Executors](https://developer.android.com/reference/java/util/concurrent/Executor.html) can help.

## Leaks
You must remember to run close() on all [Closeable](https://developer.android.com/reference/java/io/Closeable.html) objects. Android can and will do it for you, but calling close() explicitly is faster. Also be aware that repeated configuration changes, such as when a user rotates their phone, can cause leakage. Leaking Activities can be fixed by removing all references to the Activity's UI when the Activity goes off-screen.
