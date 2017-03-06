**WORK IN PROGRESS**

##Xaml Analysis

*Use the Xaml analyser to spend less time debugging and see Xaml errors in-editor*

##Introduction
It's common that xaml issues in Xamarin.Forms applications are undetected until runtime or worse, when sent out to a client. MFractor solves this by detecting Xaml issues *immediately* and then marking them inside the xaml editor with a concise error message.

Bye bye Xaml bugs! 👋

##Under The Hood

Let's take a look at what happens "under the hood" in MFractor when you open a Xaml document:

![xaml analysis flow](/img/forms/xaml-analysis-flow.png)

When you open a Xaml file that's part of a .NET project, Xamarin Studio notifies MFractor that a new Xaml document was opened for editing. MFractor will  inject the Xaml analyser into the Xaml editor and consume the Xaml document.

Once MFractor has a copy of the Xaml DOM, it *symbolicates* the xaml document. In this step all Xaml nodes are resolved to their corresponding .NET class, all attributes are resolved to properties, fields or methods and all markup extension expressions are parsed.

It may take a little while for MFractor to parse and symbolicate the Xaml DOM the first time a solution opens. While it's consuming the Xaml document, you might see a tooltip informing you that MFractor is not quite ready to analyse the document:

![xaml document parsing](/img/forms/doc-parsing.png)

When the Xaml document has been parsed and symbolicated, MFractor will analyse the document for a range of code issues. Any issues that are found are marked as either

A full list of available Xaml analysers can be found at [Xamarin.Forms Analysers](tools-in-depth/analysers.md).

Whenever you edit a Xaml code file, MFractor will cancel any running analysis, re-parse and symbolicate the document and then re-run the xaml analyser against your xaml.

##Code Fixes
When MFractor detects a code issue, it is usually able to suggest a fix as well. When MFractor can fix an issue, the squiggle beneath that issue will be yellow like so:

You can action this fix by right clicking on the text area marked by the yellow squiggle

See [Code Actions](code-actions.md) for further documentation on using Xaml to C# code generation.

##Expression Analysis



##Binding Expression Analysis
