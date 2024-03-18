# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. Begin
2. Create a new Android project in Android Studio.
3. Design the layout with an EditText for entering the URL and a Button for navigation.
4. In the XML layout file:
   - Define an EditText with an id (e.g., editTextURL).
   - Define a Button with an id (e.g., buttonNavigate).
5. In the MainActivity.java file:
   - Initialize views by finding them using findViewById().
   - Set an OnClickListener for the button.
   - Inside the OnClickListener, get the URL entered in the EditText.
   - Create an Intent with action Intent.ACTION_VIEW and parse the URL.
   - Set the Intent's data with the URL.
   - Use try-catch block to catch ActivityNotFoundException.
   - Start the activity with the created Intent.
6. Run the application on an emulator or a physical device.
7. Enter a valid URL (e.g., "www.gmail.com") in the EditText.
8. Click the "Navigate" button.
9. The system should open the URL in a web browser using Implicit Intents.
10. End




## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:THIRUMURUGAN O T
Registeration Number : 212221040171
*/
```
## ActivityMain.XML:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Implicit_Intent"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="176dp"
        android:text="Click to next"
        app:layout_constraintBottom_toBottomOf="parent"
        tools:layout_editor_absoluteX="142dp" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="268dp"
        android:ems="10"
        android:inputType="text"
        android:text="EditText"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity.Java

package com.example.implicit_intent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });

    }
}

## OUTPUT

![implicit](https://github.com/Thirualpha/ImplicitIntent-MAD/assets/113031702/fb65fd65-2683-4cae-bfbb-2ab7f75d9447)



![implicitop](https://github.com/Thirualpha/ImplicitIntent-MAD/assets/113031702/e16b0228-67f8-4558-90e1-b93bb8ea53d5)


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


