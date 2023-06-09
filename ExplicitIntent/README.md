# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

step1:Create the first activity with a layout that includes an EditText for number input and a
Button for the Factorial action.
step2:Implement an OnClickListener for the Factorial button that retrieves the number from
the EditText, calculates its factorial, and creates an Intent to open the second activity.
step3:Pass the calculated factorial value as an extra data in the Intent.
step4:In the second activity, retrieve the factorial value from the Intent using
getIntent().getIntExtra() method.
step5:Update the layout of the second activity to display the factorial value.
step6:Declare the second activity in the AndroidManifest.xml file.
step7:Build and run the application to test the functionality of both screens.


## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:Vijayalakshmi Punyala
Registeration Number :212221040134
*/
```
**MainActivity.java:**

package com.example.experiment_3;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity 
{

    Button button;
    EditText editText;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText =findViewById(R.id.editText);
        button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout

    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:ems="10"
        android:importantForAutofill="no"
        android:inputType="text"
        android:minHeight="48dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.589"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.476"
        tools:ignore="LabelFor,TextFields,SpeakableTextPresentCheck" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="156dp"
        android:layout_marginTop="172dp"
        android:text="@string/app_name"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.53" />
        
</androidx.constraintlayout.widget.ConstraintLayout>

## OUTPUT:

![2023-06-08 (16)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/3b5aee89-d8df-4b30-a514-44b5b7c27f60)


![2023-06-08 (15)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/6a4602c0-1008-4c9e-9a8b-b90bbbc13762)


![2023-06-08 (14)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/3cd2b029-9efa-4b44-868a-e31be71298f9)


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


