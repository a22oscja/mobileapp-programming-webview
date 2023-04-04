
# Rapport

to start out, the name of the app was changed by changing the variable
"app_name" in strings.xml

then a webview was created on the screen instead of the textview with the following code:
```
<WebView
        android:id="@+id/my_webview"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
as can be seen in the code, the id for the webview is "my_webview",
with its width and height matching the parent, which is the program as a whole in this case

A webview was declared in the java file to then, upon the program opening,
get linked to the webview created in the last step as using findviewbyid.
Javascript is also enabled on the webview.
The following code does all this, it can be found in the OnCreate method:
```
    myWebView = findViewById(R.id.my_webview);
    myWebView.setWebViewClient(new WebViewClient());
    myWebView.getSettings().setJavaScriptEnabled(true);
```

Lastly a very simple html page was created, before the precreated dropdown menu
was implemented using the ShowInternalWebPage and ShowExternalWebPage methods using loadUrl.
The internal brings you to the simple html page and the external page brings you to bing.
