---
title: Google I/O Connect 2023
tags: [Google I/O,Android]
style: border
color: primary
description: A Google I/O 2023 dissection.
---

# 🤔 Conference purpose

[Google I/O Connect 2023](https://rsvp.withgoogle.com/events/ioconnect-amsterdam) is an in-person developer event series hosted by Google, focused on applying and discussing the technology and announcements from [Google I/O 2023](https://io.google/2023/).
It serves as a platform for developers to gain a deeper understanding of Google products, services, and platforms through hands-on learning experiences, Q&As, demos, code labs, office hours, and more.

[Google I/O Connect](https://rsvp.withgoogle.com/events/ioconnect-amsterdam) allows software engineers and individuals in technical roles from Europe, the Middle East, and Africa to engage with Google experts, explore the content shared at Google I/O, and receive in-person guidance on how to apply those technologies effectively.

The conference aims to empower attendees to enhance their skills, expand their knowledge of Google's offerings, and build innovative solutions using Google's platforms and services. It offers a unique opportunity to interact with like-minded professionals, network with industry experts, and gain valuable insights into the future of Google's technology ecosystem.

# 🔎 Google I/O 2023 dissection

As previously mentioned, this conference’s main objective is to bring developers up to speed on the announcements of [Google I/O 2023](https://io.google/2023/).
For that reason, it was crucial to dissect it, in order to take the most out of this conference.

## New UI Page design

New UI page design guide, to help designers transition to Large Screen - https://developer.android.com/design/ui  

## Accessibility

### Increased supported font-size

Android 14 will allow users to increase font size to 200%

### Introduction of a new security flag

Added new flag for sensitive fields - android:accessibilityDataSensitive=”yes” - To not allow screen readers to have access to sensitive fields/buttons;

## Now In Android

### Passkeys

Added new sign-in method Passkeys.

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/hqdefault.jpg)](https://www.youtube.com/clip/UgkxQhk0jvL-rDNHt6OaYNC7YHSeFSbc2QaD)


### Activity Embedding

Activity embedding looks promising;

https://www.youtube.com/clip/UgkxjIS5rPgk-WJ40dx3OJaaA8CZ9EPcQh_P

 

### Gradle upgrades

Gradle upgrades that decrease project build time;



### Large Screens - Letterboxing

Large Screen in Android 14+ will no longer support Portaint-only apps



   

### Large Screens - Camera/Foldable

Folding in or out a foldable device while using the camera can lead to issues.





## Building for Android’s Future



### Predictive Back

Added new feature. It can be interesting to use instead of the “Leave the App confirmation dialog”;





### Themed Icons

Support for themed App Icons that adjust according to device’s Theme;



 

### Grammatical Inflection AKA Gendered Grammatic



 

App Action - Google Assistant

We could potentially use App Actions for more complete integration with Google Assistant;



 

Kotlin 2.0 Compiler

Kotlin compiler can decrease significantly build time;



 

 Google I/O 2023 Connect Report

Large Screens

Google’s mobile product seems to be shifting towards Large Screens (Foldables + Tablets) Why?

Foldable Screens are reaching good quality levels;

Tablets and Foldables are becoming more popular;

Most companies - such as ourselves - focus on a Portain experience, neglecting this growing market;

With the increase of the Large Screen market cap, it is a great opportunity for Apps to take advantage of the possibility of a more complete experience due to the increased screen size; e.g. Gmail (image below);



Letterboxing

It was mentioned on Now in Android section, that from Android 14+ it will no longer be possible to force Apps to be used in Portrait or Landscape only more for Large screen devices (Foldables + Tablets)

At the conference, we were able to download the Farfetch Android App and try it out on the newly released Google Tablet. We tried it in Landscape mode, and below is the result we obtained.



Letterboxed Farfetch App

Because this is a major concern for us, we discussed this topic at length with a few Googlers, and this is what we found:

We asked if there would be a way to “opt-out” being letterboxed in this Transition phase, and the answer was “Maybe” - The Googler didn’t know for sure if that was being worked on, but didn’t seem hopeful;

Neglecting the potential issues that could arise from these changes - Discussions revealed that there are easier ways to support Landscape. These easier ways (of course) do not take advantage of the increased screen size;

Camera/Foldable Opening

In Foldables with Android 14+ there is a new Camera-related concern, that was described in the Large Screens - Camera/Foldable section. This issue is due to Hardware - Google tried to patch it, but unsuccessfully;

To deal with this issue, google created 2 Support Libraries - CameraX for Jetpack and Camera2 for XML projects (like ours).

This affects us directly due to our Card Scanner feature. We use Card IO library. This is a concert, due to the fact that the Card IO library is not being updated, since early 2019;

Activity side-by-size (AKA Embedded Activities)

The usefulness of this feature can be debated at first because communication between these activities would be limited - thus it would possibly be better to have adjacent fragments;

A possible use case the Googler provided was embedding activities from other providers. A simple use-case for us would be to have a Click-and-Collect feature, where we would embed on the side a Google Maps activity, where we send a deeplink with the geographical location of the place where the user would collect the product;

AI

Google is eager to push its AI into the market (even opened an acceleration program for AI companies that will use BardAI).

AI will be integrated into multiple Google tools and services - e.g. Google Assistant, Google search, etc.

Accessibility

A lot of emphasis was placed on Accessibility - Talk Back (Android’s Screen reader for visually impaired users), Accessibility Scanner (Google App that can be used to scan Apps, to check for Accessibility-related improvements.), etc.

Interesting statistic -  around 80% of Apps have broken deeplinks, and most of them do not explore App Actions yet.

Compose

A lot of new Jetpack Compose features and SDKs:

CameraX SDK (for Foldables Support);

New Widgets SDK;

SDK for Cross-Device experiences;

…

A lot of effort is being placed into Compose.

Widgets

New Widget library for compose.

Devs report having a lot of pain points when building complex Widgets.

Cross-device experiences

New SDK was launched to make it easier to share experiences between nearby devices.



Tracking

A known pain point we have is our tracking architecture. After lengthy discussions with a very experienced Googler (who worked on Meta, Amazon, and now Google), all the companies he worked in, had huge pain points around tracking. I don’t think there is a Utopian approach where we have clean tracking. All we can do is just analyze it in depth and improve where we can.

Others

Themed icons are easy wins, companies are implementing them;

Related to translations validations - Discussed with the team behind Google Sheets, and their will soon implement the History feature for App Scripts;

Related to Google’s team’s structure/environment - Discussed the company’s values, and conversations moved towards the great read below  

https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html?smid=wa-share
