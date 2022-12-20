---
layout: post
title: Open a Password-Protected PDF in .NET MAUI PDF Viewer | Syncfusion
description: Learn here about opening a password-protected document in Syncfusion .NET MAUI PDF Viewer (SfPdfViewer) control and more.
platform: MAUI
control: SfPdfViewer
documentation: ug
---

# Open a Password-Protected PDF in .NET MAUI PDF Viewer (SfPdfViewer)

To open a password-protected or encrypted PDF document, you can use the `LoadDocument()` method by providing the password along with the document source. The following code example explains the same.

{% tabs %}
{% highlight c# %}
string password = "PASSWORD";
pdfViewer.LoadDocument(pdfDocumentStream, password);
{% endhighlight %}
{% endtabs %}

In the above code snippet, `pdfDocumentStream` is the `Stream` instance read from the encrypted PDF, and `password` is the key with which the PDF is encrypted.

## Detecting a password-protected document

You can identify whether a PDF document to be opened is a password protected or not by using the `PasswordRequested` event. This event triggers when the document to be loaded in the `SfPdfViewer` requires a password. In this event handler method, you can set the `password` property from the `PasswordRequestedEventArgs` with the correct password to load the document. Refer to the following code example.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfPdfViewer x:Name="PdfViewer" DocumentSource="{Binding PdfDocumentStream}" PasswordRequested ="PdfViewer_PasswordRequested">
{% endhighlight %}

{% highlight c# %}
public MainPage()
{
    InitializeComponent();
    Stream pdfDocumentStream = this.GetType().Assembly.GetManifestResourceStream("PdfViewerExample.Assets.Password_Protected.pdf");
    PdfViewer.DocumentSource = pdfDocumentStream;
}

private void PdfViewer_PasswordRequested(object sender, PasswordRequestedEventArgs e)
{        
    e.Password = "PASSWORD";
    e.Handled = true;
}
{% endhighlight %}
{% endtabs %}

## Handling invalid password

The `DocumentLoadFailed` event triggers when any password-protected document is loaded with a wrong or invalid password. You can handle the functionality based on your needs within this event handler method.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfPdfViewer x:Name="PdfViewer " DocumentSource="{Binding PdfDocumentStream}" PasswordRequested ="PdfViewer_PasswordRequested" DocumentLoadFailed="PdfViewer_DocumentLoadFailed">
{% endhighlight %}

{% highlight c# %}
public MainPage()
{
    InitializeComponent();
    Stream pdfDocumentStream = this.GetType().Assembly.GetManifestResourceStream("PdfViewerExample.Assets.Password_Protected.pdf");
    PdfViewer.DocumentSource = pdfDocumentStream;
}

private void PdfViewer_PasswordRequested(object sender, PasswordRequestedEventArgs e)
{        
    e.Password = "WRONG PASSWORD";
    e.Handled = true;
}

private void PdfViewer_DocumentLoadFailed(object sender, Syncfusion.Maui.PdfViewer.DocumentLoadFailedEventArgs e)
{        
    if (e.Message == "Can't open an encrypted document. The password is invalid.")
    {
        DisplayAlert("Incorrect Password", "The password you entered is incorrect. Please try again.", "OK");
    }
}

{% endhighlight %}
{% endtabs %}

The example project to open a password-protected document with a customized password request view can be downloaded [here](https://github.com/SyncfusionExamples/maui-pdf-viewer-examples). 