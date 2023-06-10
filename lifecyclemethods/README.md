# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by:Vijayalakshmi Punyala
Registeration Number :212221040134
*/
```
**MainAcitvity.java:**

package com.example.experiment_1;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.widget.Toast;

public class MainActivity extends AppCompatActivity 
{

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast.makeText(this, "onCreate Called", Toast.LENGTH_SHORT).show();
    }
    @Override
    protected void onRestart(){
        Toast.makeText(this, "onRestart Called", Toast.LENGTH_SHORT).show();
        super.onRestart();
    }
    @Override
    protected void onStart(){
        Toast.makeText(this, "onStart Called", Toast.LENGTH_SHORT).show();
        super.onStart();
    }
    @Override
    protected void onResume(){
        Toast.makeText(this, "onResume Called", Toast.LENGTH_SHORT).show();
        super.onResume();
    }
    @Override
    protected void onPause(){
        Toast.makeText(this, "onPause Called", Toast.LENGTH_SHORT).show();
        super.onPause();
    }
    @Override
    protected void onStop(){
        Toast.makeText(this, "onStop Called", Toast.LENGTH_SHORT).show();
        super.onStop();
    }
    @Override
    protected void onDestroy(){
        Toast.makeText(this, "onDestroy Called", Toast.LENGTH_SHORT).show();
        super.onDestroy();
    }
}

**activity_main.xml:**
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        android:textSize="20dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:ignore="SpUsage,TextSizeCheck" />
</androidx.constraintlayout.widget.ConstraintLayout>


## OUTPUT:

![2023-06-08 (1)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/23843f48-d075-4308-a61c-5180ba40f531)


![2023-06-08 (2)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/2ffed0d9-e0ec-4b5a-8db6-3e5f7e1b8b8c)


![2023-06-08 (3)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/90fa8b79-31c2-4fc7-ab8d-27e75bf24e02)


![2023-06-08 (5)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/4aa53bb5-8861-46ec-a9ab-9779305ad990)


![2023-06-08 (7)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/d98d230e-bf7a-4799-9ee3-f621360adace)


![2023-06-08](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/c407331d-379f-4624-9da4-7d8199734d32)



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
