---
layout: post
title: Notes on React Native Migration, from Android@Scale
share-img: "martyav.github.io/img/softserveTwilight.jpg"
---

On January 31, [Yang Mou](http://www.yzmou.com/) of [Oscar Health](https://www.hioscar.com/ny) gave a talk at the [Android@Scale](https://atscaleconference.com/events/android-scale-2018/) conference in Manhattan. He discussed migrating mobile apps to [React Native](https://facebook.github.io/react-native/). These are my notes from this session. 

***

Oscar is a health insurance company that has a small team of engineers running their mobile and web frontends and backends in-house. Most of their engineers are fullstack, and work on multiple platforms at once. They use Javascript for frontend and Python for backend work.

Because they are a small team and are maintaining apps for iOS, Android, and the web, as well as running a backend API, React Native was enticing to the engineers at Oscar Health. React Native is cross-platform, offers better ergonomics than the Android SDK, and uses Javascript, a language the whole team was familiar with. 

The original impetus was an engineer who wanted to work on the iOS app, but who didn't know Objective-C or Swift. React Native allowed them to build a feature out with a minimum of overhead. 

React Native offers a few other advantages. For example, it's much faster to reload some Javascript than to recompile a pure native app, so you save a lot of time when building. Testing is faster and easier than when using native Android tools. Finally, many web developers already know React, so they pick up on React Native relatively quickly.  

However, there are also disadvantages to working with React Native. For example, devs who come to it from a mobile background learn it slower than those who have a background in web...so if your team makeup is different from Oscar Health's, onboarding may be slower.  

Even if your team has a web-based background, they can't get away from learning some native, because sometimes you need to use native-only APIs, or performance requirements force you to drop down a layer in abstraction and write pure native code.  

React Native is also newer and less battle-tested than pure native code, and the codebase is constantly changing, requiring frequent updating (something Swift devs may sympathize with). It's also worth noting that React Native's support for Android lags behind its support for iOS, so newer features and bug fixes don't reach Android quite as quickly.

One seeming disadvantage of working with React Native can actually be handled fairly easily. Although Javascript is untyped, you can add something like type safety by using [Flow](https://flow.org/) or [Typescript](https://www.typescriptlang.org/). Flow has the advantage of looking a bit similar to Kotlin.

When developing an Android app in React Native, you can use [CSS Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) to write all your layout code in one file, rather than having it spread across multiple XML files and Activities. The syntax is very similar to writing a [LinearLayout](https://developer.android.com/guide/topics/ui/layout/linear.html).

Instead of [custom Views](https://developer.android.com/training/custom-views/index.html), React Native has components (not to be confused with how Android uses the term). You can see some examples of the concept and implementation [here](https://github.com/shoutem/ui).

React Native uses a unidirectional data flow, a little like Spotify's framework [Mobius](https://github.com/spotify/mobius) (also discussed at the conference earlier that day). Views emit events, which feed back into the controller, triggering an update of the model. Oscar uses [Redux](https://redux.js.org/) to implement this in their apps.

Because iOS, Android, and React Native all have very different ways of handling navigation between screens, the most platform agnostic approach is to use URIs, with any data being passed inside the URI as a query. This approach gives you a similar navigation scheme both across platforms, and within apps that are partially written in pure native and partially written in React Native. 

For hybrid apps, you can have an if-else statement to detect if the next screen is in React Native or something else. Navigating backward is simplified by the fact that both Android and iOS use stacks to implement a navigation history, whereas React Native uses a Javascript array.

Yang Mou recommends that if you are migrating, you write as much code is possible, front and backend, in React Native. Start with the "leaf screens" — the parts of the app that at the tips of the userflow tree. Then work backward. There will be a performance hit going from a screen that's pure native to one that's written in React Native, so avoid forcing the user to go back and forth between the two where possible. 

As you continue to migrate your app, write all new features in React Native. Try to use crossplatform APIs as much as you can, because it will save you time and simplify maintaining all your apps. And only write pure native code when performance is absolutely critical, or when you absolutely must use a native-only API.
