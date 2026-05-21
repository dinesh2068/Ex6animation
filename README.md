# Ex.No: 6 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.

## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Studio and then click on File → New → New Project.

Step 2: Then type the Application name as “Animation” and click Next.

Step 3: Then select the Minimum SDK as required and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design the layout in activity_main.xml with an ImageView and buttons for Move, Blink, Fade, Clockwise, Zoom, and Slide animations.

Step 6: Create separate animation XML files inside the res/anim/ folder for each animation and implement the logic in MainActivity.java to load and start each animation using AnimationUtils.

Step 7: Save and run the application to see different animations applied to the ImageView.


## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: DINESHKARTHIK N
Registeration Number : 212223220021
*/
```

#### MainActivity.java
```
package com.example.ex6animation;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.Button;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    ImageView imageView;
    Button btnMove, btnBlink, btnFade, btnClockwise, btnZoom, btnSlide;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        imageView = findViewById(R.id.imageView);
        btnMove = findViewById(R.id.btnMove);
        btnBlink = findViewById(R.id.btnBlink);
        btnFade = findViewById(R.id.btnFade);
        btnClockwise = findViewById(R.id.btnClockwise);
        btnZoom = findViewById(R.id.btnZoom);
        btnSlide = findViewById(R.id.btnSlide);

        btnMove.setOnClickListener(v -> startAnimation(R.anim.move));
        btnBlink.setOnClickListener(v -> startAnimation(R.anim.blink));
        btnFade.setOnClickListener(v -> startAnimation(R.anim.fade));
        btnClockwise.setOnClickListener(v -> startAnimation(R.anim.clockwise));
        btnZoom.setOnClickListener(v -> startAnimation(R.anim.zoom));
        btnSlide.setOnClickListener(v -> startAnimation(R.anim.slide));
    }

    private void startAnimation(int animResId) {
        Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), animResId);
        imageView.startAnimation(animation);
    }
}
```	

#### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:src="@drawable/ic_launcher_foreground"
        android:layout_marginBottom="30dp" />

    <Button
        android:id="@+id/btnMove"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Move" />

    <Button
        android:id="@+id/btnBlink"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Blink" />

    <Button
        android:id="@+id/btnFade"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Fade" />

    <Button
        android:id="@+id/btnClockwise"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Rotate Clockwise" />

    <Button
        android:id="@+id/btnZoom"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Zoom" />

    <Button
        android:id="@+id/btnSlide"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Slide" />

</LinearLayout>
```

## OUTPUT

<img width="457" height="836" alt="image" src="https://github.com/user-attachments/assets/98f0b9a6-8a2c-45dc-9e0d-8580ac38a821" />

<img width="488" height="846" alt="image" src="https://github.com/user-attachments/assets/da875319-8b7c-467e-b706-e8858aa96875" />


## RESULT
Thus an application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio is developed and executed successfully. 
