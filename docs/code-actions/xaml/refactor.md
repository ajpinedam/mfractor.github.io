## Extract Attribute Value Into Property Binding

**Configuration Id: com.mfractor.code_actions.forms.extract_into_property_binding**

When a Xaml attribute is initialised by a literal value (rather than an expression), this refactoring action allows a developer to extract that literal value as a property into the binding context and replace the attribute initialiser with a binding expression.

For example, given the attribute initialiser `Text=\"Hello Xamarin.Forms!\"`, this refactoring would generate a user named property (EG: Message) in the binding context, initiliase it with the string literal `\"Message\"` and replace the attribute value with the binding expresion `{Binding Message}`.";

![Extract value into property binding](/img/code-actions/forms/extract-property-binding.gif)

### Uses:

 * [Generate Instance Property](/code-generation/csharp.md#generate-instance-property)


## Rename Xaml Namespace

**Configuration Id: com.mfractor.code_actions.forms.rename_xaml_namespace**

The **Rename Xaml Namespace** code action will perform a symbolic rename-refactor on a particular Xaml within your document.

This is handy as you can then rename namespaces in a document without using a Find+Replace action; the rename xaml namespace action works against symbols so it will always rename only the namespace symbols.

To action this refactoring:

 * Within a Xaml document right click or `Alt+Return` on an `xmlns` attribute (EG: `xmlns:local="clr-namespace:myApp"`)
 * Select **Refactor**.
 * Then **Rename Namespace**.
 * Enter a new namespace name when prompted and then click enter.

Your new namespace will be applied across the document:

![Renaming a Xamarin.Forms Xaml namespace](/img/code-actions/forms/rename-xaml-namespace.gif)

### Uses:

 * [Rename Xaml Namespace Generator](/code-generation/xaml.md#rename-xaml-namespace-generator)


## Edit Color Declaration

**Configuration Id: com.mfractor.code_actions.forms.edit_inline_color**

The **Edit Color Declaration** code actions allows visual editing of colors from your Xaml.

Simply right click on a Xaml node that is a `System.Drawing.Color` or `Xamarin.Forms.Color` and select **Edit Color**. Then you can use the color picker dialog to select a new color value:

![Edit colour refactoring action](/img/code-actions/forms/edit-color.gif)

