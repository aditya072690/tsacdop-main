[![Tsacdop Banner][]][google play]

[![github action][]][github action link]
[![GitHub Release][]][github release - recent]
[![Github Downloads][]][github release - recent]
[![Localizely][]][localizely - website]
[![style: effective dart][]][effective dart pub]
[![License badge][]][license]
[![fdroid install][]][fdroid link]

## About

Enjoy podcasts with Tsacdop.

Tsacdop is a podcast player developed with Flutter, a clean, simply beautiful, and friendly app, which is also free and open source.

Credit to the Flutter team and all involved plugins, especially [webfeed](https://github.com/witochandra/webfeed), [Just_Audio](https://pub.dev/packages/just_audio), and [Provider](https://pub.dev/packages/provider).

The podcast search engine is powered by, [ListenNotes](https://listennotes.com) & [PodcastIndex](https://podcastindex.org/).

## Features

* Podcast group management
* Playlists support
* Sleep timer / speed setting
* OPML file export and import
* Auto-syncing in the background
* Listening and subscription history record
* Dark mode / accent color
* Download for offline play
* Auto-download new episodes / auto-delete outdated downloads
* Settings backup
* Skip silence
* Boost volume

More to come...

## Preview

| Home Page | Group | Podcast | Episode| Dark Mode |
| ----- | ----- | ----- | ------ | ----- |
|![][Homepage ScreenShot]|![][Group Screenshot] | ![][Podcast Screenshot] | ![][Episode Screenshot]| ![][Darkmode Screenshot] |

## Build

1. If you don't have Flutter SDK installed; Please visit the official [Flutter][Flutter Install] site.
2. Fetch the latest source code from the master branch.

``` 
git clone https://github.com/stonega/tsacdop.git
```

``` dart
final environment = {"apiKey":""};
```

3. Run the app with Android Studio or Visual Studio. Or the command line.

``` 
flutter pub get
flutter run
```
## Architecture

### Plugins

* Local storage
  + sqflite
  + shared_preferences
* Audio
  + just_audio
  + audio_service
* State management
  + provider
* Download
  + flutter_downloader
* Background task
  + workmanager

### Directory Structure

``` 
UI
src
└──home
   ├──home.dart [Homepage]
   ├──searc_podcast.dart [Search Page]
   └──playlist.dart [Playlist Page]
└──podcasts
   ├──podcast_manage.dart [Group Page]
   └──podcast_detail.dart [Podcast Page]
└──episodes
   └──episode_detail.dart [Episode Page]
└──settings
   └──setting.dart [Setting Page]

STATE
src
└──state
   ├──audio_state.dart [Audio State]
   ├──download_state.dart [Episode Download]
   ├──podcast_group.dart [Podcast Groups]
   ├──refresh_podcast.dart [Episode Refresh]
   └──setting_state.dart [Setting]

Service
src
└──service
   ├──api_service.dart [Podcast Search]
   ├──gpodder_api.dart [Gpodder intergate]
   └──ompl_builde.dart [OMPL export]
```

## Known Issue

* Playlist is unstable
  
## Getting Started with Flutter

This project is a starting point for a Flutter application.

Here are a few resources to get you started if this is your first Flutter project:

* [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
* [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials, samples, guidance on mobile development, and a full API reference.

[Flutter Install]: https://flutter.dev/docs/get-started/install
[build status - cirrus]: https://circleci.com/gh/stonega/tsacdop/tree/master.svg?style=shield
[github action]: https://github.com/stonega/tsacdop/workflows/Flutter%20Build/badge.svg
[github release]: https://img.shields.io/github/v/release/stonega/tsacdop
[fdroid install]: https://img.shields.io/f-droid/v/com.stonegate.tsacdop?include_prereleases
[fdroid link]: https://f-droid.org/en/packages/com.stonegate.tsacdop/
[localizely - website]: https://localizely.com/
