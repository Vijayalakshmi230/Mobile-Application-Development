# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Studio and click on "File" -> "New" -> "New Project".

Step 2 Design the layout by adding GUI components like buttons, text views, etc., and assign
appropriate IDs to them.

Step 3: Add a button for colors and a button for fonts, and set their respective click listeners.

Step 4: In the click listener for the color button, prompt the user to select a color and change
the background color of a specific view or the entire layout based on the user's selection.

Step 5: In the click listener for the font button, prompt the user to select a font and change the
font of a specific view or the entire layout based on the user's selection.

Step 6: In the MainActivity.java file, implement the logic to display a message when the
application starts.

Step 7: Save the changes and run the application on an Android device or emulator.

Step 8: Verify that the application launches successfully and displays the message.



## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by:VijayaLakshmi Punyala
Registeration Number :212221040134
*/
```
**MainActivity.java:**

package com.example.experiment_2;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;

import android.graphics.Typeface;

import android.os.Bundle;

import android.widget.Button;

import android.widget.TextView;

public class MainActivity extends AppCompatActivity 
{

    int ch = 1;
    float font = 30;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView t = findViewById(R.id.textView);
        TextView t1 = findViewById(R.id.textView2);
        TextView t2 = findViewById(R.id.textView3);
        TextView t3 = findViewById(R.id.textView4);
        TextView t4 = findViewById(R.id.textView5);
        Button b1 = findViewById(R.id.button1);
        b1.setOnClickListener(view -> {
            t.setTextSize(font);
            t1.setTextSize(font);
            t2.setTextSize(font);
            t3.setTextSize(font);
            t4.setTextSize(font);
            if (font == 50) {
                font = 30;
            } else {
                font += 5;
            }
        });
        Button b2 = findViewById(R.id.button2);
        b2.setOnClickListener(v -> {
            switch (ch) {
                case 1:
                    t.setTextColor(Color.RED);
                    t1.setTextColor(Color.RED);
                    t2.setTextColor(Color.RED);
                    t3.setTextColor(Color.RED);
                    t4.setTextColor(Color.RED);
                    break;
                case 2:
                    t.setTextColor(Color.GREEN);
                    t1.setTextColor(Color.GREEN);
                    t2.setTextColor(Color.GREEN);
                    t3.setTextColor(Color.GREEN);
                    t4.setTextColor(Color.GREEN);
                    break;
                case 3:
                    t.setTextColor(Color.BLUE);
                    t1.setTextColor(Color.BLUE);
                    t2.setTextColor(Color.BLUE);
                    t3.setTextColor(Color.BLUE);
                    t4.setTextColor(Color.BLUE);
                    break;
                case 4:
                    t.setTextColor(Color.CYAN);
                    t1.setTextColor(Color.CYAN);
                    t2.setTextColor(Color.CYAN);
                    t3.setTextColor(Color.CYAN);
                    t4.setTextColor(Color.CYAN);
                    break;
                case 5:
                    t.setTextColor(Color.YELLOW);
                    t1.setTextColor(Color.YELLOW);
                    t2.setTextColor(Color.YELLOW);
                    t3.setTextColor(Color.YELLOW);
                    t4.setTextColor(Color.YELLOW);
                    break;
                case 6:
                    t.setTextColor(Color.MAGENTA);
                    t1.setTextColor(Color.MAGENTA);
                    t2.setTextColor(Color.MAGENTA);
                    t3.setTextColor(Color.MAGENTA);
                    t4.setTextColor(Color.MAGENTA);
                    break;
            }
            ch++;
            if (ch == 7) {
                ch = 1;
            }
        });
        Button b3 = findViewById(R.id.button3);
        b3.setOnClickListener(v -> {
            switch (ch) {
                case 1:
                    t1.setTypeface(null, Typeface.BOLD);
                    t.setTypeface(null, Typeface.BOLD);
                    t2.setTypeface(null, Typeface.BOLD);
                    t3.setTypeface(null, Typeface.BOLD);
                    t4.setTypeface(null, Typeface.BOLD);
                    break;
                case 2:
                    t1.setTypeface(null, Typeface.ITALIC);
                    t.setTypeface(null, Typeface.ITALIC);
                    t2.setTypeface(null, Typeface.ITALIC);
                    t3.setTypeface(null, Typeface.ITALIC);
                    t4.setTypeface(null, Typeface.ITALIC);
                    break;
                case 3:
                    t.setTypeface(null, Typeface.BOLD_ITALIC);
                    t1.setTypeface(null, Typeface.BOLD_ITALIC);
                    t2.setTypeface(null, Typeface.BOLD_ITALIC);
                    t3.setTypeface(null, Typeface.BOLD_ITALIC);
                    t4.setTypeface(null, Typeface.BOLD_ITALIC);
                    break;
                case 4:
                    t.setTypeface(null, Typeface.NORMAL);
                    t1.setTypeface(null, Typeface.NORMAL);
                    t2.setTypeface(null, Typeface.NORMAL);
                    t3.setTypeface(null, Typeface.NORMAL);
                    t4.setTypeface(null, Typeface.NORMAL);
                    break;
            }
            ch++;
            if (ch == 5) {
                ch = 1;
            }
        });
    }
}

**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">
    <TextView
        android:id="@+id/textView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="center"
        android:text="Student Details"
        android:textSize="25sp"
        android:textStyle="bold"
        tools:ignore="HardcodedText" />
    <TextView
        android:id="@+id/textView2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="left"
        android:text="Name:Vijaya Lakshmi"
        android:textSize="25sp"
        android:textStyle="bold"
        tools:ignore="HardcodedText,RtlHardcoded" />
    <TextView
        android:id="@+id/textView3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="left"
        android:text="Reg_NO:212221040134"
        android:textSize="25sp"
        android:textStyle="bold"
        tools:ignore="HardcodedText,RtlHardcoded" />
    <TextView
        android:id="@+id/textView4"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="left"
        android:text="Department:CSE"
        android:textSize="25sp"
        android:textStyle="bold"
        tools:ignore="HardcodedText,RtlHardcoded" />
    <TextView
        android:id="@+id/textView5"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="left"
        android:text="Year:2nd Year"
        android:textSize="25sp"
        android:textStyle="bold"
        tools:ignore="HardcodedText,RtlHardcoded" />
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="horizontal">
        <Button
            android:id="@+id/button1"
            android:layout_width="108dp"
            android:layout_height="wrap_content"
            android:layout_margin="18dp"
            android:text="size"
            android:textSize="14sp"
            tools:ignore="ButtonStyle,HardcodedText" />
        <Button
            android:id="@+id/button2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_margin="18dp"
            android:text="color"
            android:textSize="14sp"
            tools:ignore="ButtonStyle,HardcodedText" />
        <Button
            android:id="@+id/button3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_margin="18dp"
            android:text="Style"
            android:textSize="15sp"
            tools:ignore="ButtonStyle,HardcodedText" />
    </LinearLayout>
</LinearLayout>

## OUTPUT:


![2023-06-08 (8)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/8dfedf57-fd34-4298-8f10-6dbe56c281c9)

![2023-06-08 (9)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/b115b846-43ae-40a1-bc29-48389f6ab16e)

![2023-06-08 (11)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/cdd949a2-9ded-4d47-8d80-cda5fbc05529)

![2023-06-08 (13)](https://github.com/Vijayalakshmi230/Mobile-Application-Development/assets/127175503/7487ecce-7045-407f-a796-e332a98a2ec2)




## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


