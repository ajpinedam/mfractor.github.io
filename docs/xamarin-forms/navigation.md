**WORK IN PROGRESS**

##Navigation

*Move efficiently through a Xamarin.Forms project with rich Xaml code navigation*

##Introduction
MFractor enriches the navigation between C# and Xaml code by adding a few handy shortcuts. We can:

 * Quickly cycle between views, code behind classes and view models with the Mvvm shortcuts.
 * Jump to .NET symbols from Xaml with Go-To Symbol support.
 * Hover over any xaml element to see a .NET tooltip along with its included documentation
 * Preview images through image tooltips when we hover over an image source value.

##Mvvm Navigation
When MFractor can [implicitly resolve the View - Code Behind Class - ViewModel relationship](configure-binding-context.md#implicit-binding-context-resolution), the Mvvm navigation shortcut suite is activated.

We can access these shortcuts by right clicking in a **.xaml**, **.xaml.cs** or **ViewModel.cs** code file:

 * Go To Code-Behind Class: Jumps you to the code behind class related to a view or view model
 * Go To View Model: Jumps you to the view model related to a view or code behind class.
 * Go To Xaml View: Jumps you to the xaml view related to a view model or code behind class.

 For example:


##Xaml Go-To Symbol


##Xaml Tooltips


##Image Tooltips
