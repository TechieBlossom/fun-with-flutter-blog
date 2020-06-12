+++
categories = []
date = ""
description = ""
draft = true
slug = ""
tags = []
thumbnail = ""
title = "Provider with StateNotifier"
type = ""

+++
In this video we will take a look at the State_Notifier and Flutter_State_notifier packages.

As a demonstration we will create a counter application.

A simple example, but if you stick to the end of the video you will see all of the benefits that StateNotifier can provide, as well as appreciate its simplicity.

Please note that this video assumes you are familiar with Provider and understand what a ChangeNotifier and ValueNotifier is.

If you are not familiar with Provider and ChangeNotifier then I recommend you first watch my video on Provider basics.

Or you can take a look at the written tutorial for this video which provides links to the relevant resources and information you need.

But as a quick summary a ValueNotifier is a ChangeNotifier that holds a single value.

> When value is replaced with something that is not equal to the old value as evaluated by the equality operator ==, this class notifies its listeners.

So what is the stateNotifier package?

StateNotifier re-implements ValueNotifier outside of Flutter.

To quote the documentation:

> Extracting ValueNotifier outside of Flutter in a separate package has two purposes:

* It allows Dart packages with no dependency on Flutter to use these classes. **This means that we can use them on AngularDart for example.**
* It allows solving some common problems with the original ChangeNotifier/ValueNotifier and/or their combination with provider.

This second bullet is what we are really interested in. The bit that says "their combination with provider".

By using state_notifier instead of the original ValueNotifier, we get a lot of benefits:

* A significant simplification of the integration with [**provider**](https://pub.dev/packages/provider)
* Simplified testing/mocking
* Improved performances on `addListener` & `notifyListeners` equivalents.
* Extra safety through small API changes

In this tutorial, we will also use the flutter_state_notifier package which add extra Flutter bindings to StateNotifier. This package is what allows us to integrate StateNotifier with Provider and with our widgets.

With the summary out of the way. Let's start the coding example.