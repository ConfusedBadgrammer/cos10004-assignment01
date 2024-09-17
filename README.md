<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stopwatch Circuit Assignment Readme</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #333;
        }
        ul {
            margin: 0;
            padding-left: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Stopwatch Circuit Assignment Readme</h1>
        
        <h2>Overview</h2>
        <p>This assignment involves implementing a stopwatch interface using Logisim Evolution 3.8.0. The interface is provided as a Logisim file named <code>main.circ</code>. You are required to build your solution using this file and adhere to the constraints and stages outlined below.</p>
        
        <h2>Logisim Version</h2>
        <ul>
            <li><strong>Required Version</strong>: Logisim Evolution 3.8.0</li>
            <li><strong>Download Link</strong>: <a href="https://github.com/logisim-evolution/logisim-evolution/releases">Logisim Evolution 3.8.0</a></li>
        </ul>
        <p>Ensure compatibility with this version to avoid issues with testing.</p>
        
        <h2>Allowed Components</h2>
        <p>You are permitted to use the following Logisim components:</p>
        <ul>
            <li><strong>Logic Gates</strong>: Any</li>
            <li><strong>Flip Flops</strong>: JK, D, S-R, T</li>
            <li><strong>LEDs</strong></li>
            <li><strong>Clock</strong>: Only one</li>
            <li><strong>Hex Digit Display</strong>: Provided in the interface</li>
            <li><strong>Buttons</strong>: Provided in the interface</li>
            <li><strong>Pins</strong>: For connecting circuits</li>
            <li><strong>Constants</strong>: For setting inputs that will not change</li>
            <li><strong>Splitter</strong>: For using HEX Digit Display</li>
        </ul>
        <p><strong>Note</strong>: The use of any other components, such as pre-built circuits like registers or shift registers, will result in penalties.</p>
        
        <h2>Assignment Stages</h2>
        <p>The assignment is divided into stages, each contributing to the overall grade. Complete each stage in order and save your files with the naming convention <code>stageX.circ</code>.</p>
        
        <h3>Stage 1: Implement the Start/Stop Button (10%)</h3>
        <ul>
            <li>Wire a circuit that toggles between Start and Stop states using the provided Start/Stop button.</li>
            <li>Use a Flip Flop to track the current state.</li>
            <li>Ensure the "Clock Started" LED is ON when in the Start state and OFF when in the Stop state.</li>
        </ul>
        
        <h3>Stage 2: Implement a Single Digit “Seconds” Display (15%)</h3>
        <ul>
            <li>Replace the flashing LED with a counter that increments the seconds display by 1s (0-9) every clock tick.</li>
            <li>The display should start at “00” when the Start/Stop button is first pressed.</li>
            <li>The display should stop when the Start/Stop button is pressed in the Start state and resume counting when pressed in the Stop state.</li>
        </ul>
        
        <h3>Stage 3: Implement the Full Two-Digit “Seconds” Display (20%)</h3>
        <ul>
            <li>Expand the display to show seconds in both units and tens columns (00-59).</li>
            <li>Reset the display to “00” when the Reset button is clicked and ensure the stopwatch enters the Stop state.</li>
            <li>Prevent illegal values (e.g., hex values or digits above “5” in the tens column).</li>
        </ul>
        
        <h3>Stage 4: Implement the “Minutes” Display (15%)</h3>
        <ul>
            <li>Implement a two-digit minutes display (00-99).</li>
            <li>The minutes display should increment when the seconds display wraps back to “00”.</li>
            <li>Ensure the Start/Stop and Reset buttons function correctly for the minutes display.</li>
        </ul>
        
        <h3>Stage 5: Implement the “Split” Button (15%)</h3>
        <ul>
            <li>Implement a “Split” display to show the time when the Split button is pressed.</li>
            <li>The Split Time display should remain unchanged until the Split button is pressed again or the Reset button is clicked.</li>
            <li>Reset the Split Time display to “00:00” when the Reset button is pressed.</li>
        </ul>
        
        <h3>Stage 6: Implement “Split” Time Recording and Multi-“Split” Display (15%)</h3>
        <ul>
            <li><strong>Part 6A</strong>: Record up to 5 split times when the Split button is pressed, using Flip Flops for storage. Display the most recent split time and reset all split times to 0 when the Reset button is pressed.</li>
            <li><strong>Part 6B</strong>: When in the Stop state, display each split time in turn on the Split Time display when the Split button is pressed, wrapping back to the earliest split time after showing the most recent one.</li>
        </ul>
        
        <h3>Stage 7: One Display for Everything (10%)</h3>
        <ul>
            <li>Combine all split times and elapsed time into the single “Elapsed Time” display.</li>
            <li>Display split times and elapsed time on the same display when the stopwatch is in the Stop state.</li>
            <li>Indicate when a Split time is being displayed using an additional LED.</li>
        </ul>
        
        <h2>Submission</h2>
        <p>Submit the following via Canvas (Assignment 1):</p>
        <ul>
            <li><strong>Logisim File</strong>: <code>main.circ</code> implementing the most complete version of your assignment.</li>
            <li><strong>Stage Files</strong>: Separate Logisim files for each stage, named <code>stageX.circ</code>.</li>
            <li><strong>Report</strong>: A document (Word or PDF) of up to 5 pages including:
                <ul>
                    <li>Your name, student number, unit code, and lab session</li>
                    <li>Description of the circuit</li>
                    <li>Design outline for each stage completed</li>
                    <li>Assumptions made</li>
                    <li>Any unresolved problems</li>
                    <li>Screenshots of your working circuit for each stage</li>
                </ul>
            </li>
        </ul>
        <p><strong>Late Submission</strong>: A 10% deduction per day applies for late submissions.</p>
    </div>
</body>
</html>
