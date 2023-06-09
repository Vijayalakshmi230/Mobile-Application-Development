# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by:Vijayalakshmi Punyala
Registeration Number : 212221040134
*/
```
**MainActivity.java:**

package com.example.experiment_8;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.Gallery;

import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {
    Gallery simpleGallery;
    CustomizedGalleryAdapter customGalleryAdapter;
    ImageView selectedImageView;
    int[] images = {
            R.drawable.img, R.drawable.img_1, R.drawable.img_7,
            R.drawable.img_2, R.drawable.img_8,
            R.drawable.img_3, R.drawable.img_4, R.drawable.img_5, R.drawable.img_6,
            R.drawable.img_3,
            R.drawable.img_4, R.drawable.img, R.drawable.img_1, R.drawable.img_7,
            R.drawable.img_2, R.drawable.img_5,};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
        selectedImageView = (ImageView) findViewById(R.id.imageView);
        simpleGallery.setAdapter(customGalleryAdapter);
        simpleGallery.setOnItemClickListener((parent, view, position, id) -> {
            selectedImageView.setImageResource(images[position]);
        });
    }
}
**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical">
    <ImageView
        android:id="@+id/imageView"
        android:layout_width="fill_parent"
        android:layout_height="288dp"
        android:scaleType="fitXY" />
    <Gallery
        android:id="@+id/languagesGallery"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="100dp"
        android:animationDuration="2000"
        android:padding="10dp"
        android:spacing="5dp"
        android:unselectedAlpha="50" />
</LinearLayout>


## OUTPUT


![Screenshot 2023-06-09 143759](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/fecff532-60ba-428d-9e54-8fd71beeb5cb)



## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


