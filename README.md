Download Link: https://assignmentchef.com/product/solved-ecse211-lab-5-ballistic-launcher
<br>
.Design objectives

<ol>

 <li>To design a ping-pong ball launching device capable of launching a ball into a 30 cm by 30 cm area at least 120 cm from the release point of the device 95% of the time (see <strong>Figure 1</strong>).</li>

 <li>Provide mobility for this device by mounting on a suitably modified two-wheeled robot.</li>

</ol>

Figure 1. Example map

<h1>Design requirements</h1>

The following design requirements must be met:

<ul>

 <li>The system must satisfy the design requirements from Lab 4 with respect to localization, with the following exceptions:

  <ul>

   <li>You must follow the (<strong>X</strong>,<strong>Y</strong>,<strong>θ</strong>) convention specific to this lab (refer to <strong>Figure 2</strong>).</li>

   <li>You are free to use either rising or falling edge localization.</li>

   <li>You are <strong>not</strong> required to provide a way of selecting rising or falling edge.</li>

   <li>You do <strong>not</strong> have to wait for user input after completing ultrasonic or light localization.</li>

  </ul></li>

 <li>You must allow for the following data to be entered using either the buttons and LCD display OR an easily modifiable section in your code:</li>

</ul>

<ol>

 <li>The coordinates of the Target point (<strong>Tx,Ty</strong>).</li>

</ol>

<ul>

 <li>Your robot will start in Corner 0 (0,0), localize, and then proceed to a suitable launch point for getting the ball to the specified target point. Note: the launch point chosen must be no closer than 120cm (4 tiles).</li>

 <li>Your robot must complete its demonstration procedure in a maximum of 5 minutes.</li>

</ul>

<h1>Method</h1>

<ul>

 <li>Using the kit parts available, build a ping-pong ball launching mechanism. You may also use string and elastic bands, but may not modify any kit parts.</li>

 <li>Test your device by launching ping-pong balls onto the field or floor tiles with it and measuring their (x, y) landing position relative to some target point (i.e. a nearby grid line intersection): o Determine the center of the landing positions, , by taking the mean of</li>

</ul>

the landing positions:

<ul>

 <li>Then, compute the standard deviation of the landing positions:</li>

</ul>

<ul>

 <li>If , then the required 95% success rate is</li>

</ul>

achieved.  If not, modify your design and repeat testing.

Demonstration

The design must satisfy the requirements by completing the demonstration outlined below.

Design presentation

Before demoing the design, your group will be asked some questions for approximately 5 minutes. You will present your design (hardware and software) and answer questions to test your understanding of the lab concepts. Grades will apply to the entire group, although TAs reserve the right to grade individually if they deem it necessary.

You must present your workflow, an overview of the hardware design, and an overview of the software functionality. Visualizing software with graphics such as flowcharts is valuable.

<h3>Stationary Launch</h3>

Manually place your robot at the optimal launch position relative to the target point specified by the TA.  Demonstrate your design by launching five (5) ping-pong balls from a distance at least 120 cm from the target tile and hitting the same 30 cm by 30 cm tile each time.  Your demo grade will be equal to your success rate (2 points for each ball landing within the target tile). Be sure to record launch position and the point at which the ping-pong ball first hits the ground.

One of the challenges here is determining the landing position of the ball to a reasonable degree of accuracy.  Prior to demonstrating in the lab, you should perform experiments to gather enough sample data to yield reliable statistics.  You may be asked to present this data as part of your demonstration.

<h3>Mobile Launch</h3>

In this demonstration you will place your robot in Corner 0 and key in (or hard code) the target position specified by the TA.  Set up your program to wait for the press of the Center button before localizing and navigating to the computed launch position.  Your display should clearly show the coordinates of both the launch and target positions before the button is pressed.  Once the button is pressed, your robot should proceed to the launch point, stop, issue a long BEEP, and then proceed to launch the ball.

Design your code so that once a ball is launched, the machine stops to allow manual reloading.  Pushing the Center button should initiate a pause for 5 seconds (to allow the vehicle to stabilize from the button press) followed by a launch.  This process repeats until the program is halted.  As with the stationary launch, your score is determined by your success rate (3 points for each ball landing within the target tile).

Provided materials

<strong>Sample code </strong>

No sample code is provided for this lab.

Physical material

You will be issued with a set of ping-pong balls. Other material (e.g. plastic bands) to be provided by the team.

<h1>Implementation instructions</h1>

The implementation of this lab is at your discretion. Since this lab will be done in conjunction with the entire design team, you have the opportunity to explore different solution approaches.

<h1>Report Requirements</h1>

The following sections must be included in your report. Answer all questions in the report and copy them into your report. For more information, refer to <u>ECSE211SubmissionInstructions.pdf</u>. Always provide justifications and explanations for all your answers.

<h2>Section 1: Design Evaluation</h2>

You should concisely explain the overall design of your software and hardware. You must present your workflow, an overview of the hardware design, and an overview of the software functionality. You must briefly talk about your design choices before arriving at your final design. Visualizing hardware and software with graphics (i.e. flowcharts, class diagrams) is valuable.

<h2>Section 2: Test Data</h2>

This section describes what data must be collected to evaluate your design requirements. Collect the data using the methodology described below and present it in your report.

<strong>Stationary Launch </strong><em>(20 independent trials) </em>

<ul>

 <li>Collect a minimum of 20 ball positions recorded as (x, y) coordinates.</li>

 <li>The launch position must be a minimum of 4 tiles distant from the target.</li>

 <li>You might consider using cellphone video to record the landing position of the balls.</li>

</ul>

<strong>Mobile Launch </strong><em>(10 independent trials) </em>

<ul>

 <li>Collect a minimum of 10 ball positions starting from localization.</li>

 <li>For each trial, record the actual launch position in addition to the ball position at landing</li>

</ul>

<h2>Section 3: Test Analysis</h2>

<h3>Stationary Launch</h3>

<ul>

 <li>Calculate the mean and standard deviation of the target error from your observations of landing position.</li>

 <li>Assuming that the error is drawn from a normal distribution, determine the 95% confidence interval for your launcher in the stationary case.</li>

 <li>Show the above as a plot.</li>

</ul>

<strong>Mobile Launch </strong>

<ul>

 <li>Repeat the above analysis.</li>

</ul>




<h2>Section 4: Observations and Conclusions</h2>

<ul>

 <li>Which statistic is most closely related to the repeatability of your mechanism?</li>

 <li>Would you expect this statistic to be sensitive to error in launch position? If so why; if not, why not?</li>

 <li>Using the statistical model (above) you computed for your stationary launcher, determine the probability of a successful hit, for a confidence interval of +/- 15cm. How does this compare to your actual success rate.</li>

 <li>Repeat for the case of the mobile launcher.</li>

</ul>

<h2>Section 5: Further Improvements</h2>

<ul>

 <li>Given your observations, what changes to your design would likely improve the repeatability of your results?</li>

 <li>The alternative to modifying the design is to consider a strategy that increases the likelihood of success. Given the statistics determined for your launcher in both the stationary and mobile cases, calculate the minimum number of launches required to guarantee at least one successful hit for each case.  (Hint: Binomial Distribution).</li>

</ul>

<h1>Frequently asked questions (FAQ)</h1>




<ol>

 <li><strong>What happens if the field test run takes longer than 5 minutes?</strong></li>

</ol>

The TA will conclude your demo at the 5-minute mark and will award 0 points for all the remaining, incomplete parts.


