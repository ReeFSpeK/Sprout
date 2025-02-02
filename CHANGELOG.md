* 1.0 - March 1, 2013
 * Initial public release.
* 1.1 - September 20, 2013
  * Added dynamic log level support.
  * Added basic app, device, and OS logging functionality.
* 1.2 - February 13, 2014
  * Fixing use of TestFlightLogger
* 1.2.1 - March 11, 2014
  * Fixing deadlock issue when logging exceptions.
* 1.3 - May 20, 2014
  * Making Sprout "cross platform" (iOS and OSX).
  * Added documentation for Podfile `post_install` hook and preprocessor definitions.
  * Added documentation for `CustomLogFormatter` format.
* 2.0 - August 12, 2014
  * Added Crashlytics logging support.
  * Now dynamically install optional framework loggers (TestFlight, Crashlytics)
  * Removed now unused `TESTFLIGHT` preprocessor directive.
  * Added capability to override the default loggers.
  * Added capability to override the default log formatter.
  * Renamed `CustomLogFormatter` to `SproutCustomLogFormatter`.
  * Added documentation for new features.
* 2.0.1 - August 13, 2014
  * Adding provisions for calling any previously installed exception handler.
  * Avoiding namespace conflicts for exception and signal handlers.
* 2.0.2 - August 13, 2014
  * Adding empty strings to TestFlight weak constants to avoid weak linking issues.
* 2.0.3 - October 3, 2014
  * Adding ability to override default static log level by defining `SPROUT_LOG_LEVEL`.
  * Cleaning up preprocessor macro checking and defines.
  * Adding Sprout-internal log category.
* 2.0.4 - October 17, 2014
  * Armoring against NULL backtrace symbols.
* 2.0.5 - February 5, 2015
  * Fixing TARGET_OS_MAC conditional compilation.
  * Adding `deviceName` to `logAppAndDeviceInfo` output.
* 2.0.6 - February 19, 2015
  * Adding `deviceMachine` to `logAppAndDeviceInfo` output.
* 2.0.7 - March 17, 2015
  * Removing `TestFlightLogger` as it is no longer relevant.
  * Exposed additional internals such as app and device info methods.
* 2.0.8 - June 26, 2015
  * Reimplementing backtrace functions.
  * Adding tests for backtrace funciton.
* 2.0.9 - October 16, 2015
  * Changing build project and directory structure.
  * Updated copyright and Readme.
  * Added Travis.ci build/test automation.
* 2.0.10 - November 9, 2015
  * Adding `SproutDDLogAdditions.h` with synchronous and asynchronous "log always" macros.
* 2.1 - December 7, 2015
  * Removing `logsAsZippedData` and dependency on [SSZipArchive](https://github.com/ZipArchive/ZipArchive).
* 2.2 - August 4, 2016
  * Adding code to condense instances of the same kind of signal into one, within a 1 second threshold.
* 3.0 - December 28, 2016
  * Updated to use CocoaLumberjack 3.0
  * Updated license.
* 3.1 - February 22, 2017
  * Provided block based configuration (instead of overrides)
  * Updated `logFiles` method to return NSURLs (**breaking API change**)
  * Removed weak dependency on Crashlytics for logging.
  * CocoaLumberjack 3.1 dependency
* 3.1.1 - March 20, 2019
  * Added `AppCenterLogger.h/m` for logging to [App Center](https://appcenter.ms)\
* 3.1.2 - July 9, 2021
  * Incorporated PR from @gyratorycircus to "log always" app/device info at startup.
* 3.2 - 2021-09-21
  * Updated AppCenter API use to 4.3. Using DDOSLogger instead of DDTTYLogger.
* 3.2.1 - 2021-09-21
  * Updating macOS deployment target to 10.15.
* 3.2.2 - 2021-10-11
  * Adding support for WatchOS
* 3.2.3 - 2021-10-17 - @gyratorycircus
  * Skips install of fatal signal handlers which are not supported on watchOS