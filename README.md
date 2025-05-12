# ee2003-assignment-8-solved
**TO GET THIS SOLUTION VISIT:** [EE2003 # Assignment 8 Solved](https://www.ankitcodinghub.com/product/ee2003-assignment-8-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90773&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE2003 # Assignment 8 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
# Assignment 8

Synthesis

## Goals

– Run post-synthesis simulation of your design

## Given

This builds on top of assignment 6, and the test case is also the same. The `run` script firsts tests for behavioural simulation, then synthesizes, and finally runs a post-synthesis simulation. Synthesis is done using the [`yosys`](http://www.clifford.at/yosys/) open source synthesis tool. It is quite possible that this tool has somewhat different behaviour in terms of synthesis than Xilinx Vivado. For this assignment, we are going with Yosys since it is much faster and less resource intensive, and easier to install and run.

**NOTE**: In case you have got your code synthesized with Vivado but it does not pass the scripts here, they will still be considered valid submissions, but you will need to give a complete demonstration of how it synthesizes under Vivado and why it fails under Yosys.

## Details on the assignment

Most of the work is already done: you have presumably already passed assignment 6 by now. However, there is a good chance that there are problems with the code that result in synthesis errors, or possible synthesis/simulation mismatches. You need to correct these.

A few notes:

– `yosys` generates a lot of information very fast. You may want to redirect this to a file (use something like `yosys synth.ys &gt; out.log`) and go through it in case you find errors.

– Some common sources of problems:

– Latches instead of flip-flops

– Multi-driver nets: you *initialize* inside one `always` block and do the evaluation in another block.

– Look for *WARNING*s in the output of yosys: in most cases it will proceed to synthesize even when there are warnings, but the output will likely not match what you expect.

### Synthesis script

`synth.ys` is a script used by `yosys` – it uses some simple defaults to target the Xilinx 7-series FPGAs.

For reference, a `synth.tcl` script is also provided, which you should be able to use with Vivado. However, due to computational load issues, this is not going to be evaluated.

### Grading

You could possibly just submit the exact same code that you did for assignment 6. However, if there are issues with synthesis, then correct them and submit for this assignment. You will NOT be penalized for assignment 6 if the synthesis fails, but for this assignment you must pass the post-synthesis simulation.

## HowTo

Fork this repostiry (`EE2003/a8`) into your namespace so that you can edit and push changes.

The `run.sh` script performs all the steps required to compile and test your code. The `iverilog` compiler is used for running the verilog simulations. `yosys` is required for the synthesis steps. Under Ubuntu (at least 18.04+) you can just run `sudo apt install yosys` and it should work.

&nbsp;
