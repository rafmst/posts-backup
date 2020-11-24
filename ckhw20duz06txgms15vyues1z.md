## 4 benefits of using Expo

If you clicked on this article, chances are you already know what  [Expo](https://expo.io/)  is, but if actually don't know let's say it is a set of components and tools that extend React Native and facilitate the development of mobile apps with React Native.

To be fair, my first experience with React Native was through Expo so I'm a little biased.

## 1. Easy to use

For developers with zero experience in mobile app development that want to start with hybrid development, Expo is the easiest way to go. Since its actually not hybrid but real native code, it will also be very performant. Expo-cli together with all the Expo environment, makes it easy to develop an entire native app just by using Javascript, never touching any native code.

Even React Native's website sends you to the Expo way of developing. To start, its as easy as running two commands:

```bash
$ npm install -g expo-cli
$ expo init MyNewApp
```

Another way that Expo makes it easy its when using the Expo Client on your phone. The Expo Client is an app that lets you run your apps before deploying simply by scanning a QR Code. This QR Code is available in the console after running `expo start`. Personally this is great for me, I like running my prototypes directly on my phone, with live reloading included. Off course Expo doesn't bound us to the phone, we can still use the simulators or emulators and even that way we don't need any specific configuration.

## 2. From coding to shipping in a breeze

One thing I realised is that its extremely fast to deploy a project from coding, to building, to publishing its usually really fast. Mainly for two reasons, first you never worry about iOS/Android differences if you have an application that doesn't require complex things, and the second reason is just because you don't really care about building, everything is done in the Expo servers. Yes, this is always a con for those who like to have more control on the building process, but for the majority of apps its ok and its actually faster. 

## 3. Libraries & documentation

There is a ton of libraries available developed and curated by Expo, and when there isn't there is always some alternative library that works with Expo because now most of developers code libraries with Expo in mind. To give some examples of the libraries available:

- `expo-battery`;
- `expo-crypto`;
- `expo-device`;
- `expo-battery`;
- `expo-haptics`;
- `expo-sensors`;
- `expo-sqlite`;
- and many others...

The documentation is also great and usually there is a dedicated page for each library made by Expo, with api references explaining all attributes and methods along with examples and how to's. It really seems like everything is covered.

## 4. Active development

The team is currently really active on the development, I feel like this was the best year for Expo development, with 3 SDK versions released and SDK 40 being released in December. The team released a statement in the start of the year about planing a quarterly release and as far as today they have been delivering it. Usually I have zero errors when updating SDK's and that is great.
