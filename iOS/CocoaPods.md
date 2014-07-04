# CocoaPods

- Dependency Management Tool

## Traditional development disadvantages

- Wasting disk space
- Versions (hard to get a specific version)
- No central place with all available libraries
- Separation of downloaded code (making changes to code makes it harder to update)

## CocoaPods to the rescue

- Helps you overcome most of the issues mentioned above
- Resolves dependencies between various libraries, fetches source code for the dependencies, creates and maintains the right environment for you to build your project with the minimum of hassles
- Instead of downloading some code from GitHub and copying to your project (thus making future updates a pain), you can let CocoaPods do it all for you!

## Let's Pod

Update Ruby (["rubyyyy, hoooovno, rubyyyyy, hoooooovnoo, hovnooo, rubyyyyyyy"](http://www.youtube.com/watch?v=P-dxpuhwJSI))

```
$ sudo gem update --system
```

Requirements:
- [Command Line Tools](https://developer.apple.com/downloads/index.action) for Xcode (Xcode > Preferences > Downloads > Components)

### Install CocoaPods

```
$ sudo gem install cocoapods
$ pod setup
```

### Search for pods

Search for pods by name or description

```
$ pod search RestKit
```

### Create Podfile

In your project directory create Podfile by

```
$ touch Podfile
```

Edit Podfile as following

```
platform :ios
pod 'RestKit', '0.9.3'
```

For more details refer to [docs](http://rubydoc.info/gems/cocoapods/Pod/Podfile)

### Install pod

```
$ pod install
```

Fetches all dependencies and dependencies of dependencies (I know, it must be aliens, right)

CocoaPods might also tell you his

```
[!] From now on use 'CocoaPodsExample.xcworkspace'
```

You're now good to go!

### Update pod

Pod install will not update your dependencies even if a new version is available

```
$ pod update
```

## Advanced

### Display more details for pod commands

You might want to show more descriptive console output while executing pod commands

For that use

```
$ pod --verbose command
```

So for example

```
$ pod --verbose update
```

## Luke, join the dark side!

Just for the comparison take a look what you would have to do if you were to use [submodules](https://github.com/RestKit/RestKit/wiki/Installing-RestKit-in-Xcode-4.x)
