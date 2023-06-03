# Ex.No:9 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “calculator operation”.
Developed by:vikas N
Registeration Number :212221040179
*/
```
##activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
android:padding="16dp"
tools:context=".MainActivity">

<EditText
    android:id="@+id/etNum1"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:hint="Enter Number 1"
    android:inputType="numberDecimal" />

<EditText
    android:id="@+id/etNum2"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:hint="Enter Number 2"
    android:inputType="numberDecimal" />

<Button
    android:id="@+id/btnAdd"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:backgroundTint="#F44336"
    android:text="Add"
    android:textColor="#FFFFFF" />

<Button
    android:id="@+id/btnSub"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:backgroundTint="#9C27B0"
    android:text="Subtract" />

<Button
    android:id="@+id/btnMul"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:backgroundTint="#FFC107"
    android:text="Multiply" />

<Button
    android:id="@+id/btnDiv"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:backgroundTint="#4CAF50"
    android:text="Divide" />

<TextView
    android:id="@+id/tvResult"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="16dp"
    android:text="Result: "
    android:textSize="18sp" />

</LinearLayout>
```
##MainActivity.java
```
package com.example.calculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

EditText num1, num2;
Button btnAdd, btnSub, btnMul, btnDiv;
TextView result;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    num1 = findViewById(R.id.etNum1);
    num2 = findViewById(R.id.etNum2);
    btnAdd = findViewById(R.id.btnAdd);
    btnSub = findViewById(R.id.btnSub);
    btnMul = findViewById(R.id.btnMul);
    btnDiv = findViewById(R.id.btnDiv);
    result = findViewById(R.id.tvResult);

    btnAdd.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            double number1 = Double.parseDouble(num1.getText().toString());
            double number2 = Double.parseDouble(num2.getText().toString());
            double sum = number1 + number2;
            result.setText("Result: " + sum);
        }
    });

    btnSub.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            double number1 = Double.parseDouble(num1.getText().toString());
            double number2 = Double.parseDouble(num2.getText().toString());
            double difference = number1 - number2;
            result.setText("Result: " + difference);
        }
    });

    btnMul.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            double number1 = Double.parseDouble(num1.getText().toString());
            double number2 = Double.parseDouble(num2.getText().toString());
            double product = number1 * number2;
            result.setText("Result: " + product);
        }
    });

    btnDiv.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            double number1 = Double.parseDouble(num1.getText().toString());
            double number2 = Double.parseDouble(num2.getText().toString());
            if (number2 != 0) {
                double quotient = number1 / number2;
                result.setText("Result: " + quotient);
            } else {
                result.setText("Cannot divide by zero");
            }
        }
    });
}
}
```
## OUTPUT

![243107336-76a53380-b6bd-4427-8fc2-32ebac6ab5b1](https://github.com/suryacse05/Mobile-Application-Development/assets/133752491/1e243e16-26f4-4c9a-8bb6-72d3085e0e23)



## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
