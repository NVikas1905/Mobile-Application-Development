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
Developed by:Akash R
Registeration Number :212221220003
*/
```
##ACTIVITY_MAIN.XML:
```
 <androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="@color/background"
tools:context=".MainActivity">
 <TextView
 android:id="@+id/textView"
android:layout_width="264dp"
android:layout_height="40dp"
android:layout_marginTop="124dp"
android:fontFamily="@font/roboto_black"
android:paddingLeft="180px"
android:paddingTop="10px"
android:paddingRight="150px"
android:paddingBottom="10px"
android:text="HELLO WORLD"
android:textColor="@color/white"
android:textSize="50px"
android:background="@color/dark"

app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/but
ton" tools:ignore="MissingConstraints" />
 <Button android:id="@+id/button"
android:layout_width="322dp"
android:layout_height="49dp"
android:layout_marginTop="144dp"
android:backgroundTint="@color/dark"
android:text="MOBILE APPLICATION
DEVELOPMENT"
app:layout_constraintEnd_toEndOf="parent"
android:textColor="@color/white"
app:layout_constraintHorizontal_bias="0.494"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
##MAINACTIVITY.JAVA
```
package com.example.exercise_01; import
androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint; import
android.os.Bundle; import android.widget.Toast; public class
MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
 Toast.makeText(getApplicationContext(), "On Create Called",
Toast.LENGTH_SHORT).show();
}
protected void onStart() {
 Toast.makeText(getApplicationContext(), "On Start Called ",
Toast.LENGTH_SHORT).show();
super.onStart();
}
protected void onRestart() {
super.onRestart();
 Toast.makeText(getApplicationContext(), "On Restart Called",
Toast.LENGTH_SHORT).show();
}
protected void onResume() {
 Toast.makeText(getApplicationContext(), "On Resume Called",

Toast.LENGTH_SHORT).show();
super.onResume();
}
protected void onStop() {
super.onStop();
 Toast.makeText(getApplicationContext(), "On Stop Called",
Toast.LENGTH_SHORT).show();
}
protected void onPause() {
super.onPause();
 Toast.makeText(getApplicationContext(), "On Pause Called",
Toast.LENGTH_SHORT).show();
}
protected void onDestroy() {
super.onDestroy();
 Toast.makeText(getApplicationContext(), "On Destroy Called",
Toast.LENGTH_SHORT).show();
}
}
```
## OUTPUT
![243109514-d7d03179-df91-478e-9670-e55b99925c71](https://github.com/suryacse05/Mobile-Application-Development/assets/133752491/4bd190d9-d26c-44ef-affd-0071b5b2f9fb)





## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
