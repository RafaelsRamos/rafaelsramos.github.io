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


## 🖌 New UI Page design

New UI page design guide, to help designers transition to Large Screen - https://developer.android.com/design/ui


## :accessibility: Accessibility


### Increased supported font-size

Android 14 will allow users to increase font size to 200%


### Introduction of a new security flag

Added new flag for sensitive fields - android:accessibilityDataSensitive=”yes” - To not allow screen readers to have access to sensitive fields/buttons;


## Now In Android


### Passkeys

Added new sign-in method Passkeys.

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/UgkxQhk0jvL-rDNHt6OaYNC7YHSeFSbc2QaD)



### Activity Embedding

Activity embedding looks promising;

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/UgkxjIS5rPgk-WJ40dx3OJaaA8CZ9EPcQh_P)



### Gradle upgrades

Gradle upgrades that decrease project build time;



### [Large Screens - Letterboxing](#-now-in-android-letterboxing)

Large Screen in Android 14+ will no longer support Portaint-only apps

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/Ugkxi1Ncg-c2ZNw0cETbprEHja9Vy0ftC-jd)

   

### Large Screens - Camera/Foldable

Folding in or out a foldable device while using the camera can lead to issues.

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/UgkxO8T4EUh06zk5eIwGi0-FMafucHr9SNes)



## Building for Android’s Future



### Predictive Back

Added new feature. It can be interesting to use instead of the “Leave the App confirmation dialog”;

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/Ugkxv27KASvtccpj1vSiPh4hvRru-Efy0i_l)




### Themed Icons

Support for themed App Icons that adjust according to device’s Theme;

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/UgkxYszZBOxN2xyvY7u-CAO-xGN4aZcSHvez)

 

### Grammatical Inflection AKA Gendered Grammatic

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/Ugkxvyjds-3bmlnu9D5k9gIIQ5Om2GWeJQ_N)

 

### App Action - Google Assistant

App Actions could be used for more complete integration with Google Assistant;

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/Ugkxc70V257yQSgoczeJ8Uff45QvU64_OsQP)



### Kotlin 2.0 Compiler

Kotlin compiler can decrease significantly build time;

[![Now In Android](https://img.youtube.com/vi/qXhjN66O7Bk/maxresdefault.jpg)](https://www.youtube.com/clip/Ugkxu6V0SyXvxvEh2nSBmzlXlSeFEQdoRsgz)

 


# 📰 Google I/O 2023 Connect Report


## Large Screens

Google’s mobile product seems to be giving more and more light over Large Screens devices (Foldables + Tablets) Why?
- Foldable Screens are reaching good quality levels;
- Tablets and Foldables are becoming more popular;
- Most companies focus on a Portain experience only, neglecting this growing market;
- With the increase of the Large Screen market cap, it is a great opportunity for Apps to take advantage of a more complete experience due to the increased screen size; e.g. Gmail (image below);

![Gmail in Large Screen landscape](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjhx53R-GbJpanWgBnk-ZopDV-DYrSj8ypqWsGzm37IRjXUrJ_fnSi4Jk9exynF609G5cZuBqnkhfL1_Zri07W1kr3xOclD-zar0m6ozQY581ym7kHxAfpKjN2iBhwfR61HG2S070A5QTrMUyY5CkE8Jbf3Lb0ZVgs8jKGVuMU-RU-ja5HkGcMJ4Nv2/s711/Gmail,%20Chat,%20and%20Meet%20experience%20on%20Android%20foldable%20devices%20and%20tablets%20.png)



## Letterboxing

It was mentioned in the [Now in Android](#-now-in-android-letterboxing) section, that from Android 14+ it will no longer be possible to force Apps to be used in Portrait or Landscape only more for Large screen devices (Foldables + Tablets) without being letterboxed.

![App being letterboxed](https://developer.android.com/static/images/guide/topics/large-screens/app-compatibility/enhanced_letterboxing.png)

Because this is an experience-breaking change, this topic was discussed at length with a few Googlers, and this is what was found:
- We asked if there would be a way to “opt-out” being letterboxed in this Transition phase, and the answer was “Maybe” - The Googler didn’t know for sure if that was being worked on, but didn’t seem hopeful;
- Neglecting the potential issues that could arise from these changes - Discussions revealed that there are easier ways to support Landscape. These easier ways (of course) do not take full advantage of the increased screen size;



## Camera/Foldable Opening

In Foldables with Android 14+ there is a new Camera-related concern, that was described in the Large Screens - Camera/Foldable section. This issue is due to Hardware - Google tried to patch it, but unsuccessfully;

To deal with this issue, Google created 2 Support Libraries - [CameraX](https://developer.android.com/jetpack/androidx/releases/camera) for Jetpack Compose projects and [Camera2](https://developer.android.com/training/camera2) for XML projects.



## Activity side-by-size (AKA Embedded Activities)

The usefulness of this feature can be debated at first because communication between these activities would be limited - thus it would possibly be better to have adjacent fragments;

A possible use case the Googler provided was embedding activities from other providers. Possible usages:
- E-Commerce company with item collection on the seller - The user can see the E-Commerce App side-by-side with Google Maps, to show where the item must be picked up;
- A Job searching company - The users can see an open job in the Job searching App side-by-side with Google Maps, to evaluate the commute that he/she would have to do if working that specific job;


## AI

Google is eager to push its AI into the market - opened an acceleration program for AI companies that use BardAI.

AI will be integrated into multiple Google tools and services - e.g. Google Assistant, Google Search, etc.

## Accessibility

A lot of emphasis was placed on Accessibility - **Talk Back** (Android’s Screen reader for visually impaired users), **Accessibility Scanner** (Google App that can be used to scan Apps, to check for Accessibility-related improvements.), etc.



## Compose

- A lot of new Jetpack Compose features and SDKs:
- CameraX SDK (for Foldables Support);
- New Widgets SDK;
- SDK for Cross-Device experiences;

A lot of effort is being placed into Compose.



## Widgets

- New Widget library for Compose.
- Devs report having a lot of pain points when building complex Widgets.



## Cross-device experiences

A new SDK was launched to make it easier to share experiences between nearby devices.



### Tracking

Tracking is an issue in almost every software. After lengthy discussions with a few Googlers, it seems like tracking is a huge pain for everyone.
I don’t think there is a Utopian approach where we have clean tracking. All one can do is analyze it in depth and improve where we can.



# Others

- Themed icons are easy wins, companies are implementing them;
- Related to Google’s team’s structure/environment - Discussed the company’s values, and conversations moved towards the great read the following [this article](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html?smid=wa-share).
