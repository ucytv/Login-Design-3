### Login-Design-3

This project consists of design only. The design which follows the trends of 2020 includes a screen that you can enter your application. The demo and source codes are shown following. Click on the link for similar designs: [Login-Design-1](https://github.com/ucytv/Login-Design-1), [Login-Design-2](https://github.com/ucytv/Login-Design-2)


### Demo
![login_design_3](https://user-images.githubusercontent.com/37077627/82720109-21e8a900-9cb9-11ea-8db6-8083dec1b77e.png)

### Dependencies
```
implementation 'com.google.android.material:material:1.1.0'
```

### Theme

```
<style name="LoginTheme" parent="Theme.MaterialComponents.DayNight">
        <item name="colorPrimary">@color/colorAccent</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
</style>
```

### Color
```
<color name="colorPrimary">#BF0B0B</color>
<color name="colorPrimaryDark">#951C1C</color>
<color name="colorAccent">#FEFFFF</color>
```

### Font
```
<font-family xmlns:app="http://schemas.android.com/apk/res-auto"
        app:fontProviderAuthority="com.google.android.gms.fonts"
        app:fontProviderPackage="com.google.android.gms"
        app:fontProviderQuery="Arsenal"
        app:fontProviderCerts="@array/com_google_android_gms_fonts_certs">
</font-family>
```

### Style

*Login Button*
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <stroke android:color="@color/colorAccent"
                android:width="2dp"/>
            <solid android:color="@color/colorAccent"/>
            <corners android:radius="4dp"/>
        </shape>
    </item>
</selector>
```

*Forgot Button*
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <stroke android:color="@color/colorAccent"
                android:width="2dp"/>
            <gradient android:startColor="@color/colorPrimaryDark"/>
            <corners android:radius="4dp"/>
        </shape>
    </item>
</selector>
```
*Circle*
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="oval">
            <stroke android:color="@color/colorAccent"
                android:width="4dp"/>
            <solid android:color="@color/colorAccent"/>
            <size android:width="80dp" android:height="80dp"/>
        </shape>
    </item>
</selector>
```

### String
```
<string name="app_name">TinyDBApp</string>
<string name="login">LOGIN</string>
<string name="user_id">User ID</string>
<string name="password">Password</string>
<string name="remember_me">Remember Me</string>
<string name="forgot_password">I forgot my password</string>
<string name="signup_question">Don\'t have an account yet?</string>
<string name="sign_up">SIGN UP</string>
```

### Java Class
```
  @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        //Must be fullscreen!
        getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN,
                WindowManager.LayoutParams.FLAG_FULLSCREEN);
        setContentView(R.layout.activity_main);

        getSupportActionBar().hide(); //This is important!
    }
```

### XML File
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:orientation="vertical"
    android:padding="60dp"
    android:background="@color/colorPrimary"
    android:theme="@style/LoginTheme"
    tools:context=".MainActivity"
    >

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="60dp"
        android:layout_gravity="center"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:fontFamily="@font/arsenal"
            android:text="LOGIN"
            android:textColor="@color/colorAccent"
            android:textSize="44sp"
            android:textStyle="bold" 
            />

        <ImageView
            android:layout_width="80dp"
            android:layout_height="80dp"
            android:layout_gravity="center"
            android:layout_marginStart="80dp"
            android:src="@drawable/blood_icon"
            android:background="@drawable/image_style"
           />

    </LinearLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:layout_marginTop="80dp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/user_id"
        android:textColorHint="@color/colorAccent"
        app:endIconMode="clear_text"
        app:endIconTint="@color/colorAccent"
        app:boxStrokeWidthFocused="2dp"
        app:boxStrokeColor="@color/colorAccent"
        app:helperTextTextColor="@color/colorAccent"
        app:hintTextColor="@color/colorAccent"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        >

        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:fontFamily="@font/arsenal"
            android:textColor="@color/colorAccent" 
            />

    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:layout_marginTop="12dp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/password"
        android:textColorHint="@color/colorAccent"
        app:hintTextColor="@color/colorAccent"
        app:helperTextTextColor="@color/colorAccent"
        app:endIconMode="password_toggle"
        app:endIconTint="@color/colorAccent"
        app:boxStrokeColor="@color/colorAccent"
        app:boxStrokeWidthFocused="2dp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox.Dense"
        >

        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:textColor="@color/colorAccent"
            android:fontFamily="@font/arsenal"
            />

    </com.google.android.material.textfield.TextInputLayout>

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="8dp"
        >

        <CheckBox
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:buttonTint="@color/colorAccent"
            android:textColor="@color/colorAccent"
            android:text="@string/remember_me"
            android:fontFamily="@font/arsenal"
            android:layout_alignParentEnd="true"
            />

    </RelativeLayout>

    <Button
        android:layout_marginTop="12dp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@drawable/button_style"
        android:textColor="@color/colorPrimary"
        android:text="@string/login"
        android:fontFamily="@font/arsenal"
        android:textAllCaps="true"
        android:textStyle="bold"
        />

    <Button
        android:layout_marginTop="16dp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@drawable/button_style_2"
        android:textSize="16sp"
        android:textColor="@color/colorAccent"
        android:layout_gravity="center"
        android:textStyle="bold"
        android:fontFamily="@font/arsenal"
        android:text="@string/forgot_password"
        android:textAllCaps="false"
        />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="12dp"
        android:layout_gravity="center"
        android:gravity="center"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textSize="15sp"
            android:textColor="@color/colorAccent"
            android:layout_gravity="center"
            android:textStyle="italic"
            android:fontFamily="@font/arsenal"
            android:text="@string/signup_question"
            />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textSize="16sp"
            android:layout_marginStart="15dp"
            android:textColor="@color/colorAccent"
            android:layout_gravity="center"
            android:textStyle="bold"
            android:fontFamily="@font/arsenal"
            android:text="@string/sign_up"
            />
    </LinearLayout>
</LinearLayout>
```
