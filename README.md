This repo holds TruClient scripts created as examples of how to create scripts on real apps.

Scripts are in various folders, one folder for each [UI feature/capability](Features.md).

Apps being tested by scripts are of two types:

A). **[Challenge pages](#ChallengeApps)** containing examples of technologies that might be encountered on real sites.
We script them to experience insight into how to script on real sites,
so that we can script real sites faster and better, while we are not in emergency mode.

B). **[Demo pages](#DemoPages)** containing a generic implementation of frameworks used to develop real apps.
We script them to provide a "heads up" on difficulties that might be encountered 
in real apps built with each framework listed here.

Scripts (and explanation of scripts) for each challenge or demo is in a separate folder in this repo.
Folder names are in brackets mentioned below.

**CAUTION: Scripts pointing to websites here should not run with more than a single user at a time.**

<hr />

# <a name="ChallengeApps"></a> Challenge apps

* <a href="#CorrelationChallenge"> **MLT1** = MyLoadTest Challenge</a>
* <a href="#TheInternet"> **TIH1** = The Internet on Herokuapp Challenge</a>


### <a name="CorrelationChallenge"></a> MLT1 = MyLoadTest Challenge
http://www.myloadtest.com/training/correlation-challenge/
was developed by LoadRunner master Stuart Moncrieff (in Melbourne, Australia)
for use with LoadRunner C-language scripting.
This was before TruClient became available.


### <a name="TheInternet"></a> TIH1 = The Internet on Herokuapp Challenge
http://the-internet.herokuapp.com/
is a website constructed by a Selenium functional test automation guru Dave Haeffner.

Source code used to build the website is at 
https://github.com/tourdedave/the-interne 
which contains instructions for creating a local server 

David uses the sample site to provide the basis for describing Selenium coding tips such as 
http://elementalselenium.com/tips/45-checkboxes.


<hr />
# <a name="DemoPages"></a> Demo JavaScript Pages/apps

The TruClient scripting technology associated with HP LoadRunner addresses apps which are driven by **JavaScript**.
(The "Mobile Application - HTTP" LoadRunner script protocol create scripts from PCAP files created by WireShark)

There are several types of demo framework samples:

* <a href="#DesktopJSFrameworkDemos"> "Responsive" web development frameworks</a>
* <a href="#HybridMobileFrameworkDemos"> Hybrid mobile app development frameworks</a>


## <a name="DesktopJSFrameworkDemos"></a> "Responsive" web development frameworks

* <a href="#Bootstrap"> Bootstrap</a>


### <a name="Bootstrap"></a> Bootstrap Responsive web developmenet framework

http://getbootstrap.com/examples/theme/
provides a demo page showing how the whole range of UI elements look when built using 
Bootstrap.JS downloaded from 
or (more commonly) referenced from a CDN in HTML.
However the page doesn't have code to respond to user actions mimic'd by TruClient automation scripts.

http://expo.getbootstrap.com/
and http://builtwithbootstrap.com/
provide a showcase of real sites built using the library. 

The library began within Twitter, and enabled made it humanly possible to create responsive websites
by changing a few HTML properties. This simplicity is made possible by limiting how much space each column
takes by allocating 12 slots among all boxes. 

Bootstrap depends on jQuery and Grunt utilities.

<!-- http://www.williamghelfi.com/blog/2013/09/12/my-first-bootstrap-theme-with-themestrap/
-->
<hr />

## <a name="HybridMobileFrameworkDemos"></a> Hybrid app development framework demos

* <a href="#Cordova"> Cordova/PhoneGap</a>
* <a href="#jQueryMobile"> jQueryMobile</a>
* <a href="#SenchaSpace"> SenchaSpace</a>
* <a href="#Trigger.io"> Trigger.io</a>
* <a href="#Worklight"> Worklight</a>
 
These frameworks create apps that don't require users to update their app.
Since JavaScript is dynamically sent from the server, apps can be updated dynamically
without re-submitting to the app store (which can take days or even not at all).

More importantly, the faster speed of development and testing shifts time to improving the UX
and better marketing.


NOTE: <a href="#Appcelerator"> Appcelerator</a> is not scripted in TruClient because the resulting app
is compiled into native code, and thus rather than JavaScript being exchanged with the server.


### <a name="Cordova"></a> Cordova/PhoneGap Demo (PGD1)

https://play.google.com/store/apps/details?id=com.dreamappworld.android.phonegapdemo.free&hl=en
Phone Gap Demo (PGD1) Android app.

http://phonegap.com 

User Interface Samples

PhoneGap (Apache Cordova) is a free and open source framework that allows you to create mobile apps using standardized web APIs.

### <a name="jQueryMobile"></a> jQueryMobile

A generic implementation of each framework feature is listed at  
http://api.jquerymobile.com/category/all/

http://demos.jquerymobile.com/1.4.5/
was the latest version listed at
http://jquerymobile.com/demos/

### <a name="SenchaSpace"></a> SenchaSpace

http://www.sencha.com/products/space/
Sencha Space does not seem to have a demo like the Kitchen Sink
for their other product.

Sencha Space is a a managed enterprise environment for securely distributing HTML5 and hybrid business apps 
in a way that offers business control of data without commandeering an employee’s phone.


### <a name="Trigger.io"></a> Trigger.io

https://trigger.io/examples/
lists mobile demo apps buildt using the 
https://trigger.io/
web-based mobile development platform and **Forge.io** replacement for PhoneGap/Coordova
that doesn't require locally installed IDE such as XCode, Eclipse.
Its UI components and cloud based build environment are a minimum of $39 per month after a 14 day trial.

<a target="_blank" href="http://trigger.io/cross-platform-application-development-blog/2012/02/24/why-trigger-io-doesnt-use-phonegap-5x-faster-native-bridge/">
The basis for the company's claims about faster performance than PhoneGap are from 2012:
<img src="http://trigger.io/cross-platform-application-development-blog/wp-content/uploads/2012/02/chart_1-21.png">
</a> using code at https://github.com/trigger-corp/Forge-vs-Cordova-Performance.

On iOS, JavaScript serializes API calls and store them temporarily in the DOM. 
It then makes a request to a fake URI (forge://…) which the native component intercepts
and acts on what is stored in the DOM.

JavaScript is called to execute directly in the context of the UIWebView by iOS component:

```
UIWebView.stringByEvaluatingJavaScriptFromString
```

### <a name="Worklight"></a> Worklight from IBM
http://www-01.ibm.com/software/in/worklight/
IBM Worklight is part of IBM calls its MobileFirst platform that 
extends PhoneGap (Apache Cordova) with additional development tools and server support for backend integration, authentication, push notifications, and life cycle management. 

[This article in Stackoverflow](http://stackoverflow.com/questions/12403319/why-use-ibm-worklight-if-it-ultimately-uses-phonegap?utm_source=appsebook&utm_medium=ebook&utm_campaign=MoovwebKinveyEbook)
notes that Worklight access more native controls than PhoneGap 
(Options Menu, busy indicator, tabbars, etc).

<hr />

### <a name="Appcelerator"></a> Appcelerator (ACL1)

uses its Aptana IDE to develop JavaScript, which is compiled into native code.


