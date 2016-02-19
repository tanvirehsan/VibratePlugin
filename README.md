## Vibrate
Simple and elegant way to trigger the vibration on a device in your Xamarin, Windows, and Xamarin.Forms projects.

## Status - In Production
Build Status: [![Build status](https://ci.appveyor.com/api/projects/status/4j8dh6sofntn7494?svg=true)](https://ci.appveyor.com/project/Plugins/vibrate)

## Setup
* Available on NuGet: https://www.nuget.org/packages/Xam.Plugins.Vibrate [![NuGet](https://img.shields.io/nuget/v/Xam.Plugins.Vibrate.svg?label=NuGet)](https://www.nuget.org/packages/Xam.Plugins.Vibrate/)
* Install into your PCL project and Client projects.

**Platform Support**

|Platform|Supported|Version|
| ------------------- | :-----------: | :------------------: |
|Xamarin.iOS|Yes|iOS 7+|
|Xamarin.iOS Unified|Yes|iOS 7+|
|Xamarin.Android|Yes|API 10+|
|Windows Phone Silverlight|Yes|8.0+|
|Windows Phone RT|Yes|8.1+|
|Windows Store RT|---|8.1+|
|Windows 10 UWP|Yes|10+|
|Xamarin.Mac|No||


### API Usage

To gain access to the Vibrate class simply use this method:

```
var v = CrossVibrate.Current;
v.Vibration(1000); // 1 second vibration
```

#### Methods

```
/// <summary>
/// Vibrate the phone for specified amount of time
/// </summary>
/// <param name="milliseconds">Time in Milliseconds to vibrate. 500ms is default</param>
void Vibration(int milliseconds = 500);
```


#### Platform Tweaks

**iOS**
There is no API to vibrate for a specific amount of time, so it will vibrate for the default time the system specifies (around 500 milliseconds..

**Android**
The `android.permission.VIBRATE` permission will automatically be added for you into your AndroidManifest.xml


#### Contributors
* [jamesmontemagno](https://github.com/jamesmontemagno)

Thanks!

#### License
The MIT License (MIT)
Copyright (c) 2016 James Montemagno / Refractored LLC
