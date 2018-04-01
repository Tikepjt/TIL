# Table or Grid

***

## (편법)리니어레이아웃에 리니어 레이아웃을 넣고 자식의 웨이트를 1로 준다.

* ex)01
  리소스는 대강 넣은 뒤 실제 사진으로 대체 예정

  ```
  <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="horizontal"
    tools:context="com.example.tike_pjt.egk_productlist.SplashActivity">


    <LinearLayout
        android:layout_width="0dp"
        android:layout_height="match_parent"
        android:layout_weight="1"
        android:orientation="vertical">

        <ImageButton
            android:id="@+id/imageButton1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton3"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton4"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="0dp"
        android:layout_height="match_parent"
        android:layout_weight="1"
        android:orientation="vertical">

        <ImageButton
            android:id="@+id/imageButton5"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton6"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton7"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton8"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="0dp"
        android:layout_height="match_parent"
        android:layout_weight="1"
        android:orientation="vertical">

        <ImageButton
            android:id="@+id/imageButton9"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton10"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton11"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />

        <ImageButton
            android:id="@+id/imageButton12"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            app:srcCompat="@android:drawable/alert_light_frame" />
    </LinearLayout>

</LinearLayout>
  ```
