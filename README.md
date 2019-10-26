 -------------------------Java file---------------------------------
 Toolbar toolbar;
 
  @Override
    protected void onCreate(Bundle savedInstanceState) {
    toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
        
        getSupportActionBar().setDisplayHomeAsUpEnabled(true);
        getSupportActionBar().setDisplayShowHomeEnabled(true);
  }
  
  @Override
    public boolean onSupportNavigateUp() {
        onBackPressed();
        return true;
    }
    
-------------------------XML file---------------------------------

      <androidx.appcompat.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="?attr/actionBarSize"
        android:layout_alignParentStart="true"
        android:background="@color/colorPrimary"
        app:layout_collapseMode="pin"
        app:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
        app:popupTheme="@style/AppTheme.PopupOverlay">


        <TextView
            android:id="@+id/tv_toolbar_name"
            android:layout_width="wrap_content"
            android:layout_height="?attr/actionBarSize"
            android:layout_gravity="center"
            android:layout_marginRight="@dimen/_2sdp"
            android:gravity="center"
            android:text="Kitchen"
            android:textColor="#fff"
            android:textSize="@dimen/_16sdp"
            android:textStyle="bold" />
    </androidx.appcompat.widget.Toolbar>
    
-------------------------Manifest file------------------------------
    <activity
            android:name=".TableDetailsActivity"
            android:launchMode="singleTop"
            android:screenOrientation="portrait"
            android:theme="@style/AppTheme.NoActionBar" />
            
            
-------------------------Style file------------------------------

    <style name="AppTheme.NoActionBar">
        <item name="windowActionBar">false</item>
        <item name="windowNoTitle">true</item>
    </style>
