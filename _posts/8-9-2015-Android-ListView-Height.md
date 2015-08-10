---
layout: post
title: Android ListView Set Height Properly
description: Proper way to set ListView height to fill its container
modified: 2015-9-8
category: android
tags: [Android, Software, ListView]
comments: true
share: true
featured: true
---

# The layout

{% highlight XML %}
	<LinearLayout
   		xmlns:android="http://schemas.android.com/apk/res/android"
    	android:layout_width="match_parent"
    	android:layout_height="fill_parent"
    	android:orientation="vertical" >

    	<ListView
        	android:id="@+id/android:list"
	        android:layout_width="match_parent"
    	    android:layout_height="0dp"
        	android:layout_weight="1"/>

	</LinearLayout>
{% endhighlight %}

# Java