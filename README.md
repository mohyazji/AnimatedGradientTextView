![alt tag](https://cloud.githubusercontent.com/assets/12541829/19215982/51424130-8dad-11e6-8a5f-e92652e4ce2b.gif)

AnimatedGradientTextView : Color gradients for TextView
=======================================================

This library will allow you to create TextView which uses color gradients and custom fonts.

Latest release
---------------

The most recent release is v0.0.3, released October 23, 2016

To add a dependency using Gradle, add in your **top-level build.gradle**:
```
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```

And then add in your **app build.gradle** :
```
dependencies {
	compile 'com.github.mursaat:animatedgradienttextview:v0.0.3'
}
```

Getting started
---------------
 
Firstly, don't forget to add this in your **container layout** :
```xml
xmlns:app="http://schemas.android.com/apk/res-auto"
```

Here is an exemple using an **AnimatedGradientTextView**. I just put in my **xml layout** :
```xml
<com.mursaat.extendedtextview.AnimatedGradientTextView
	...
	app:colors="@array/funny_colors"
	app:simultaneousColors="4"
	app:angle="45"
	app:speed="1000"
	app:font="BebasNeue.otf" 
	/>
```


All these parameters are optionals. Some explanations :
* **colors** : It must reference an array of colors in **res/values/attr.xml**, for example :
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
	...
    <array name="funny_colors">
        <item>@color/materialRed</item>
        <item>@color/materialLime</item>
        <item>@color/materialOrange</item>
        <item>@color/materialPurple</item>
    </array>
</resources>
```

* **simultaneousColors** : The number of colors (of the array) possibly displayed in a same time
* **angle** : The angle of the color gradient
* **speed** : A number in milliseconds. Increase this number will decrease the gradient move speed
* **font** : Must be a name of a font located in **assets/fonts** folder
