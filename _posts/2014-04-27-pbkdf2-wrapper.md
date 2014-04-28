---
layout: post
title:  "PBKDF2-Wrapper"
date:   2014-04-27
categories: open-source pbkdf2 cocoapods
---

Last weekend I was messing around and [reading up](https://www.mikeash.com/pyblog/friday-qa-2012-08-10-a-tour-of-commoncrypto.html) on `CommonCrypto`, the built in encryption library for iOS and OSX.

From the docs:
> Common Crypto provides low-level C support for encryption and decryption. Common Crypto is not as straightforward as Security Transforms, but provides a wider range of features, including additional hashing schemes, cipher modes, and so on.

The way I learn learn best to actually use the tool I am trying to learn to build something meaningful. Since `CommonCrypto` is all "low-level C" I decided to take the [PBKDF2 algorithm](http://blog.agilebits.com/2011/05/05/defending-against-crackers-peanut-butter-keeps-dogs-friendly-too/) from it an build a higher level Objective C interface for it.

After some experimenting I outlined a few classes, and wrote out a consise API that provides flexibility and some additional benefits on top of the C implementation.

I was happy with how it turned out so I wrote some tests and turned it into a [`CocoaPod`](http://cocoapods.org). If you want to use it simply add `pod PBKDF2-Wrapper` to your `Podfile`.

The project is [hosted on GitHub](https://github.com/joeymeyer/PBKDF2-Wrapper) and available under the MIT License. Please feel free to experiment with it yourself and [let me know what you think](mailto:contact@joeymeyer.com).
