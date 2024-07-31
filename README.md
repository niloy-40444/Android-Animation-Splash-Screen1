# Android-Animation-Splash-Screen1
Android-Animation-Splash-Screen.....................


Android Animation
Animation in android Application is the process of Making motion and shape change. The basic ways of animation that we will look upon in this article.
Procedure

    Create or open your project in android studio.
    Create anim Driectory.
    Create animation xml.
    Simple code in java. 

Animation Path like this res > anim
animation directory in android studio - java

///////////////////////////////////////////////////////////////////////////
bottom_anim.xml
 <set xmlns:android="http://schemas.android.com/apk/res/android">  
   <translate  
     android:duration="1500"  
     android:fromXDelta="0%"  
     android:fromYDelta="-100%"  
     />  
   <alpha  
     android:duration="1500"  
     android:fromAlpha="0.1"  
     android:toAlpha="1.0"  
     />  
 </set> 
 //////////////////////////////////////////////////////////////////////////



 
///////////////////////////////////////////////////////////////////////////
top_anim.xml
 <set xmlns:android="http://schemas.android.com/apk/res/android">  
   <translate  
     android:duration="1500"  
     android:fromXDelta="0%"  
     android:fromYDelta="-50%"  
     />  
   <alpha  
     android:duration="1500"  
     android:fromAlpha="0.1"  
     android:toAlpha="1.0"  
     />  
 </set> 
 //////////////////////////////////////////////////////////////

 
//////////////////////////////////////////////////////////////
right_to_left.xml
 <translate  
     android:duration="1000"  
     android:fromXDelta="100%p"  
     android:toXDelta="0"/>  
   <alpha  
     android:fromAlpha="0.0"  
     android:toAlpha="1.0"  
     android:duration="500"  
     />  
     //////////////////////////////////////////////////////////////////


     
     
///////////////////////////////////////////////////////////////////////////
fade_in.xml

 <set xmlns:android="https://schemas.android.com/apk/res/android"  
   android:fillAfter="true" >  
   <alpha  
     android:duration="1000"  
     android:fromAlpha="0.0"  
     android:interpolator="@android:anim/accelerate_interpolator"  
     android:toAlpha="1.0" />  
 </set> 
 //////////////////////////////////////////////////////


///////////////////////////////////////////////////////////////////////////
fade_out.xml
 <set xmlns:android="https://schemas.android.com/apk/res/android"  
   android:fillAfter="true" >  
   <alpha  
     android:duration="1000"  
     android:fromAlpha="1.0"  
     android:interpolator="@android:anim/accelerate_interpolator"  
     android:toAlpha="0.0" />  
 </set> 
 /////////////////////////////////////////////////////////////////////




/////Our animation is done. now we do some code for textview or imageview./////





/////////////////////////////////////////////////////////////

Xml Code............!!!

/////////////////////////////////////////////////////////////
activity_main.xml

  <ImageView  
     android:id="@+id/logo"  
     android:layout_width="100dp"  
     android:layout_height="100dp"  
     android:layout_centerInParent="true"  
     android:src="@mipmap/ic_launcher" />  
   <TextView  
     android:id="@+id/appName"  
     android:layout_width="wrap_content"  
     android:layout_height="wrap_content"  
     android:layout_below="@id/logo"  
     android:layout_centerHorizontal="true"  
     android:layout_marginTop="10dp"  
     android:text="@string/app_name"  
     android:textColor="@color/black"  
     android:textSize="20sp" />  


///////////////////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////////




     

/////////////////////////////////////////////////////////////////////////////
   Java Code..............!!!!
/////////////////////////////////////////////////////////////////////////////
MainActivity.java

 public class Splash extends MainApp {  
   
   ImageView logo;  
   TextView appName;  
   
   Animation Splash_top,Splash_bottom;  
   
   @Override  
   protected void onCreate(Bundle savedInstanceState) {  
     super.onCreate(savedInstanceState);  
     setContentView(R.layout.activity_splash);  
   
     logo = findViewById(R.id.logo);  
     appName = findViewById(R.id.appName);  
   
     Splash_top = AnimationUtils.loadAnimation(this, R.anim.splash_top);  
     Splash_bottom = AnimationUtils.loadAnimation(this, R.anim.splash_bottom);  
   
     logo.setAnimation(Splash_top);  
     appName.setAnimation(Splash_bottom);  
   
   
   } // OnCreate Method CLose here ==============  
////////////////////////////////////////////////////////////////////////////////////////
