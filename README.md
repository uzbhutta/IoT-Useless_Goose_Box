# IoT Useless Goose Box
<!-- INTRO -->
<p>Have you ever seen one of those <a href="https://www.youtube.com/watch?v=aqAUmgE3WyM">videos</a> of a box that simply turns itself off after being turned on by a user and thought, "...How useless?"  Well we've found a way to make that box just a little less... useless!</br></br>

This year's <b>2016 EngHack Winner</b>, is a Waterloo themed <i>useless box</i> that uses an intuitive Android app to incorporate user customization.  This not only incorporates awesome IoT functionality, but additionally gives the user the power to remotely define new patterns in which the box can turn itself off; via an array of light bulbs, speakers, and servo motors.</p>

<img src="images/introPicture.jpg"/>

#Here Is How We Did It
<h2>Materials</h2>
<h4>HARDWARE</h4>
<ul>
  <li>Particle Photon</li>
  <li>Arduino Uno Kit</li>
  <li>Toggle Switch</li>
  <li>3 Relays</li>
  <li>Speaker (Goose Quacking)</li>
  <li>2 Servo Motors</li>
  <li>Mini Light bulb</li>
  <li>Flashlight</li>
  <li>Plushy Goose</li>
  <li>Wood</li>
  <li>Wood Glue</li>
  <li>Nails</li>
  <li>Soldering Iron & Solder</li>
  <li>Metal Hinges</li>
  <li>Hook</li>
  <li>Cardboard</li>
</ul>
<h4>SOFTWARE</h4>
<ul>
  <li>Android Studio: Java</li>
  <li>Particle Dev: C++/Arduino/Particle</li>
</ul>

<!-- BOX  -->
<h2>Building the Box</h2>
<img src="images/boxConstruction.jpg"/>  
<p>The box's encasing is a rectangular prism shaped wooden box.  The lid of the box was secured with hinges; allowing it to easily rotate open with a sevrvo motor.  A thicker piece of wood was used to cut out the arm that was later covered in pipe cleaners and fastened to a second servo motor.  Both servos were secured to the inside faces of the box.</br></br>

A combination of scrap wood, hot glue, and screws were used to fasten the switch, LED, light bulb, speaker, and hook to hold the goose to the inside of the box.  All parts were cut and drilled to shape using a drill press and band saw.</p>
<img src="images/hardwarePic.jpg"/>
<!-- CONTROL PROGRAM  -->
<h2>Control Program</h2>
<img src="images/DSC01584.JPG"/>
<p>The control program of the GooseBot was written in such a way that allows the user's box to open in one of two ways: with randomized patterns or patterns designed by the user. 

<h4>Main Loop</h4>
<p>A main loop is continuously run that checks whether or not the switch has been turned on.  When it has, a pattern is randomly chosen from an array of either pre-set or custom patterns and used to open the box.</p>

<h4>Pattern Definition</h4>
<p>Each pattern is a combination of 5 actions that include the actuation of the mini light bulb, flashlight, servo motors, and goose speaker. Various combinations of these actions make up the patterns the box performs before turning itslef back off. Each action can vary in the way in which it actuates as follows:</p>
<h5>Flashlight and Mini Light Bulb</h5>
<ul>
  <li>On</li>
  <li>Delayed On</li>
  <li>Off</li>
  <li>Flicker</li>
</ul>
<h5>Servo Motors for Arm and Lid</h5>
<ul>
  <li>Normal</li>
  <li>Fast</li>
  <li>Slow</li>
  <li>Shake</li>
</ul>
<h5>Goose Speaker</h5>
<ul>
  <li>On</li>
  <li>Off</li>
</ul>
<p>Each of the actuation methods corrolates to a <i>char</i> of letter <i>A</i> through <i>D</i>. When a pattern is created the 5 letters are saved as a string and added to an array of custom or pre-set patterns. The <i>main loop</i> then uses this array from which to randomly select a pattern to perform.</p>
<!--ToDo: How actions are broken down (the letter codes), how this letter string is passed into array, random index picked and run. How we wrote a suite of functions to process codes (see image of workflow) -->
<!-- ANDROID APPLICATION  -->
<h2>App</h2>
<!-- ToDo: Functionalities: add new custom rows, delete custom rows, click row in app to run row remotely, toggle between presets and custom patterns-->
