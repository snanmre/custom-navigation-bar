# custom-navigation-bar


**NOTE THAT** Changes in these files tagged with "[ADD]"

# Adding Key Buttons
 - Add buttons(com.android.systemui.statusbar.policy.KeyButtonView) into **navigation_bar.xml** files contained in;
    - res/layout/
    - res/layout-ldrtl/
    - res/layout-sw600dp/
    - res/layout-sw720dp/
 - Don't forget to define "systemui::keyCode" value.
 - Consider different rotations (FrameLayouts in navigation_bar.xml with id ```rot90``` and ```rot0```)
 - Sample: Brightness buttons (```kbBrightnessDown```, ```kbBrightnessUp```) in **navigation_bar.xml**

# Adding Custom Buttons
 - Add buttons into **navigation_bar.xml** files
 - Create a touch listener for the button in **PhoneStatusBar.java**
 - Use action ```MotionEvent.ACTION_UP``` in the listener
 - Sample: ```mStandByOnTouchListener``` in **PhoneStatusBar.java**

# Handling Buttons in Application Level
 - Create a touch listener for the button
 - Then broadcast an intent
 - Sample: ```mStandByOnTouchListener``` in **PhoneStatusBar.java**

# Hiding/Showing Navigation Bar or Enable/Disable Buttons
 - Register a broadcast intent receiver in **PhoneStatusBar.java**
 - Then process received intent data
 - Sample: ```mNavBarReceiver``` in **PhoneStatusBar.java**
