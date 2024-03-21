# Ex-No_2-Intent(Implicit & Explicit)

Develop program to perform explicit and implicit intent by creating a buttons using Android Studio

## AIM:
To develop a program to perform explicit and implicit intent by creating a buttons using Android Studio

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as Intent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Create a Layout and two buttons named as explicit intent and implicit Intent 

Step 7: By clicking Implict Intent button open google page using Implicit Intents in MainActivity file.

Step 8: By clicking Explicit Intent button open second page using Explicit Intents in MainActivity file.

Step 7: Save and run the application.


## Program:
 ```

Program to create a layout by click button option ,open google page using Implicit Intents in Android Studio. .
Developed by: HARSHITHA V
RegisterNumber: 212223230074

```

## MainActivity.java:
```
package com.example.ex_2;

import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.os.Bundle;


import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    Button explicit_btn, implicit_btn;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        explicit_btn = (Button)findViewById(R.id.explicit_Intent);
        implicit_btn = (Button) findViewById(R.id.implicit_Intent);

        //implement Onclick event for Explicit Intent

        explicit_btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                Intent intent;
                intent = new  Intent(getBaseContext(), activity_second.class);
                startActivity(intent);
            }
        });
        implicit_btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                Intent intent1 = new Intent(Intent.ACTION_VIEW);
                intent1.setData(Uri.parse("https://www.gmail.com"));
                startActivity(intent1);
            }
        });


    }
}
```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingBottom="@dimen/activity_vertical_margin"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceMedium"
        android:text="If you click on Explicit example we will navigate to second activity within App and if you click on Implicit example AbhiAndroid Homepage will open in Browser"
        android:id="@+id/textView2"
        android:clickable="false"
        android:layout_alignParentTop="true"
        android:layout_alignParentStart="true"
        android:layout_marginTop="42dp"
        android:background="#3e7d02"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Explicit Intent Example"
        android:id="@+id/explicit_Intent"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="147dp" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Implicit Intent Example"
        android:id="@+id/implicit_Intent"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true" />

</RelativeLayout>
```
## Activity_second.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent"
    android:layout_height="match_parent" android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:background="#CCEEAA"
    tools:context="com.example.android.intents.SecondActivity">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceLarge"
        android:text="This is Second Activity"
        android:id="@+id/textView"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true" />
</RelativeLayout>
```

## Activity_second.java:
```
package com.example.ex_2;
import androidx.appcompat.app.AppCompatActivity;

import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Toast;

import android.os.Bundle;


public class activity_second extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
        Toast.makeText(getApplicationContext(), "We are moved to second Activity",Toast.LENGTH_LONG).show();
    }
}
```

## OUTPUT:


![Screenshot 2024-03-21 090007](https://github.com/harshi1111/INTENT_GIT/assets/84671735/95627c77-6134-4f24-9aca-10ed7b033a2d)

![Screenshot 2024-03-21 090332](https://github.com/harshi1111/INTENT_GIT/assets/84671735/080b7efc-44df-4507-be19-2babdb28a431)


## RESULT:
Thus a Simple Android Application to open google page using Implicit Intents in Android Studio was developed and executed successfully.
