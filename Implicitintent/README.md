# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:Vikas N
Registeration Number :212221040179
*/
```
##activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<TextView
  android:id="@+id/textView"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginStart="4dp"
  android:layout_marginTop="52dp"
  android:text="@string/enter_an_url"
  android:textSize="26sp"
  app:layout_constraintStart_toStartOf="parent"
  app:layout_constraintTop_toTopOf="parent"
  tools:ignore="ExtraText" />

<EditText
  android:id="@+id/E1"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginTop="120dp"
  android:ems="10"
  android:inputType="textPersonName"
  android:text=""
  android:textColor="#2196F3"
  app:layout_constraintEnd_toEndOf="parent"
  app:layout_constraintHorizontal_bias="0.791"
  app:layout_constraintStart_toStartOf="parent"
  app:layout_constraintTop_toTopOf="parent" />
  
<Button
  android:id="@+id/button"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginBottom="484dp"
  android:text="Jump Into"
  app:backgroundTint="#4CAF50"
  app:layout_constraintBottom_toBottomOf="parent"
  app:layout_constraintEnd_toEndOf="parent"
  app:layout_constraintHorizontal_bias="0.462"
  app:layout_constraintStart_toStartOf="parent" />
 </androidx.constraintlayout.widget.ConstraintLayout>
 ```
 ## MainActivity.java
```
package com.example.intent_implementation;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
Button button;
EditText e1;
@Override
protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 button = findViewById(R.id.button);
 e1 = findViewById(R.id.E1);
 button.setOnClickListener(view -> {
     String url = e1.getText().toString();
     Intent i1 = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
     startActivity(i1);
 });
}
}
```
 
## OUPUT


![243099529-c915e17d-cf30-415b-b87e-103ec84610ed](https://github.com/suryacse05/Mobile-Application-Development/assets/133752491/e7b2407c-21a9-4573-800f-9ffa0937936d)



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


