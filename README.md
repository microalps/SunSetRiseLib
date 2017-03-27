# Sunrise and sunset calculation in C#

Heavily cleaned up and simplified C# library to calculate the sunrise and sunset for a location on earth on any given date. Compiled for .NET 4.6.2 and signed assemblies.

## Usage

```C#
// Date for which to calculate the sunrise and sunset
var date = DateTime.Today;

// Latitude for which to calculate the sunrise/sunset
var latitude = 52.3702157;

// Longitude for which to calculate the sunrise/sunset
var longitude = 4.8951679;
            
// Hours from UTC which this location is in
var utcOffset = TimeZone.CurrentTimeZone.GetUtcOffset(DateTime.Now).Hours;

// Write the output to the screen
Console.WriteLine("Date: " + date.ToLongDateString());
Console.WriteLine("UTC Offset: " + utcOffset);
Console.WriteLine("Coordinates: LONG " + longitude + " LAT " + latitude);
Console.WriteLine("Sunrise: " + SunSetRiseLib.SunriseAt(latitude, longitude, date, utcOffset));
Console.WriteLine("SunSet: " + SunSetRiseLib.SunsetAt(latitude, longitude, date, utcOffset));
```

![Sample output](./SampleOutput.png)

## NuGet

Also available as NuGet Package: [SunSetRiseLibKZ](https://www.nuget.org/packages/SunSetRiseLibKZ/)

## Version History

Version 1.1.1.0 - March 27, 2017

Changed namespace of code to make it look cleaner when used

Version 1.1.0.0 - March 27, 2017

Initial version as forked. Cleaned up code, compiled against .NET 4.6.2 and signed the assemblies.

## Credits

Forked from https://github.com/sely2k/SunSetRiseLib

## Feedback

Comments\suggestions\bug reports are welcome!

Koen Zomers
mail@koenzomers.nl