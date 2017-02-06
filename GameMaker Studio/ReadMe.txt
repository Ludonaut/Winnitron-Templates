
What was changed in the empty template project compared to a standard new project?
__________________________________________________________________________________

Global Game Settings

    /Windows/General
    - Disabled "Display the cursor"
    - Disabled "Display Splash Screen"
    
    /Windows/Graphics
    - Enabled "Start in fulscreen mode"
    - Disabled "Interpolate colors between pixels" //This can be activated again depending on the artstyle of your game
    - Enabled "Use synchronization to avoid tearing" //Can be deactivated again if screen tearing is no problem for your game and you need the slightly faster response time
    - Disabled "Allow switching to fullscreen"



Scripts

    - scr_wt_controls_update() //used by obj_wt_controler

Objects

    - obj_wt_controler
        //persistant object that needs to be placed only in the very first room 
        //handles the back button (go back to start room and end game if already in start room) 
        //updates easy to use global key variables like:
        //p1_up, p1_left, p1_down, p1_right, p1_button1, p1_button2. p2_up etc.
        //p1_up_pressed, p1_left_pressed etc.
        //p1_up_released, p1_left_released etc.

Rooms

    rm_start (settings)
    - Width: 640
    - Height: 360
    - Speed: 60
    //Just a preset resolution for a pixel art game that will scale pixel perfect on 720p, 1080p, 1440p, 2160p etc. screens and will run at 60fps
    //Can be changed freely
    - placed instance of "obj_wt_controler" in top left corner

Macros

    - Defined keyboard constants accourding to the winnitron specification for four players