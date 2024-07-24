# img_picker_platform_interface

A common platform interface for the [`img_picker`][1] plugin.

This interface allows platform-specific implementations of the `img_picker`
plugin, as well as the plugin itself, to ensure they are supporting the
same interface.

# Usage

To implement a new platform-specific implementation of `img_picker`, extend
[`ImagePickerPlatform`][2] with an implementation that performs the
platform-specific behavior, and when you register your plugin, set the default
`ImagePickerPlatform` by calling
`ImagePickerPlatform.instance = MyImagePickerPlatform()`.

# Note on breaking changes

Strongly prefer non-breaking changes (such as adding a method to the interface)
over breaking changes for this package.

See https://flutter.dev/go/platform-interface-breaking-changes for a discussion
on why a less-clean interface is preferable to a breaking change.

[1]: ../img_picker
[2]: lib/img_picker_platform_interface.dart
