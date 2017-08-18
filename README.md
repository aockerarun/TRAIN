# TRAIN
Date:18/08/17,Time:2.42
We have completed more than 30% of our of trifi project work,we are developing an android application for the society by using three types of online apk platform 
 

package com.my.newproject;

import android.app.*;
import android.os.*;
import android.view.*;
import android.view.View.*;
import android.widget.*;
import android.content.*;
import android.content.ClipboardManager;
import android.graphics.*;
import android.media.*;
import android.net.*;
import android.text.*;
import android.util.*;
import android.webkit.*;
import java.util.*;
import java.text.*;



public class MainActivity extends Activity {

        private LinearLayout linear1;
        private ImageView imageview2;
        private EditText edittext1;
        private ImageView imageview3;
        private TextView textview2;





        @Override
        protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.main);
                initialize();
                initializeLogic();
        }

        private void  initialize() {
                linear1 = (LinearLayout) findViewById(R.id.linear1);
                imageview2 = (ImageView) findViewById(R.id.imageview2);
                edittext1 = (EditText) findViewById(R.id.edittext1);
                imageview3 = (ImageView) findViewById(R.id.imageview3);
                textview2 = (TextView) findViewById(R.id.textview2);


                imageview2.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _v) {

                        }
                });
                imageview3.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _v) {

                        }
                });

        }

        private void  initializeLogic() {

        }




        // created automatically
        private void showMessage(String _s) {
                Toast.makeText(getApplicationContext(), _s, Toast.LENGTH_SHORT).show();
        }

        private int getRandom(int _minValue ,int _maxValue){
                Random random = new Random();
                return random.nextInt(_maxValue - _minValue + 1) + _minValue;
        }

        public ArrayList<Double> getCheckedItemPositionsToArray(ListView _list) {
                ArrayList<Double> _result = new ArrayList<Double>();
                SparseBooleanArray _arr = _list.getCheckedItemPositions();
                for (int _iIdx = 0; _iIdx < _arr.size(); _iIdx++) {
                        if (_arr.valueAt(_iIdx))
                                _result.add((double)_arr.keyAt(_iIdx));
                }
                return _result;
        }

}
<LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        >
        <LinearLayout
                android:id="@+id/linear1"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:padding="8dp"
                android:orientation="horizontal"
                >
                <ImageView
                        android:id="@+id/imageview2"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:src="@drawable/images"
                        android:scaleType="center"
                        />
                <EditText
                        android:id="@+id/edittext1"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="8dp"
                        android:text="medical help"
                        android:textSize="12sp"
                        android:textColor="#000000"
                        android:hint="Edit Text"
                        android:textColorHint="#607D8B"
                        />
                <ImageView
                        android:id="@+id/imageview3"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:src="@drawable/default_image"
                        android:scaleType="center"
                        />
                <TextView
                        android:id="@+id/textview2"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:padding="8dp"
                        android:text="fire"
                        android:textSize="12sp"
                        android:textColor="#000000"
                        />
        </LinearLayout>
</LinearLayout>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
        package="com.my.newproject">


    <application android:allowBackup="true"
        android:label="trifi"
        android:icon="@drawable/app_icon"
        android:name=".SketchApplication"
        android:theme="@style/AppTheme">

                        <activity
                                android:name=".MainActivity"
                                android:configChanges="orientation|screenSize"
                                android:screenOrientation="portrait"
                                >
                                <intent-filter>
                                        <action android:name="android.intent.action.MAIN"/>
                                        <category android:name="android.intent.category.LAUNCHER"/>
                                </intent-filter>
                        </activity>
                        <activity android:name=".DebugActivity" android:screenOrientation="portrait"/>
    </application>

</manifest>

if i pressed any one of the icon out of 5 icon then the information will show the information the paticular icon's function in the another page of the application
