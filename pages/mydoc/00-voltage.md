---
title: "Euclid Probe Voltages"
keywords: probe, version, voltage
tags: [FAQ]
permalink: 00-voltage.html
sidebar: mydoc_sidebar
folder: mydoc
toc: true
summary: What is the difference in voltage versions? 
---
Currently there are 2 versions of Euclid Probe kits available, 5V & 24V. There is no difference in price. The PCB's and circuitry are the same. The difference is the 24V components are bulked up to handle driving the LED's at the higher voltage.  

### Why are There Different Voltage Versions?  
The voltage only matters if you intend to illuminate the LEDs as status and function indicators and from where you get that power from- see <a href="\03_wiring.html#intermediate-wiring-led-operation-3-wire-mode">3-Wire installation.</a>  

### How to Decide Which Version to Get?  
Here is a table with criteria to consider:  

<div style="width:100%;text-align:center;">  
<table>  
<tr>  
  <td>Are you deploying to an endstop port?  
  </td>  
  <td>Are you using a remote CAN-BUS controller?  
  </td>
</tr>  
<tr>
  <td> <a href="images\04-wiring\boards_BTT\Slide5.PNG" data-lity>  
<img src="images\04-wiring\boards_BTT\Slide5.PNG" style="width:400px; border:2px solid CornflowerBlue"></a>  
  </td>
  <td><a href="images\04_CANB_example.jpg" data-lity>  
        <img src="images\04_CANB_example.jpg" style="width:400px; border:2px solid CornflowerBlue"></a>  
  </td>
</tr>
<tr>
  <td>Then all you need is the 5V version  
  </td>
  <td>Then all you need is the 5V version  
  </td>
</tr>
</table>
<p></p>

<table>
<tr>
  <td>Are you using a remote toolboard & 24V Probe Input?
  </td>
  <td>Are you using a remote toolboard and then using an endstop port?
  </td>
</tr>
<tr>
  <td><a href="images\04-wiring\boards_BTT\Slide4.PNG" data-lity>
       <img src="images\04-wiring\boards_BTT\Slide4.PNG" style="width:400px; border:2px solid CornflowerBlue"></a>  
  </td>
  <td><a href="images\04-wiring\boards_BTT\Slide3.PNG" data-lity>
        <img src="images\04-wiring\boards_BTT\Slide3.PNG" style="width:400px; border:2px solid CornflowerBlue"></a>
  </td>
</tr>
<tr>
  <td>Then all you need is the 24V version  
  </td>
  <td>Then all you need is the 24V version  
  </td>
</tr>
</table>
</div>

### How to tell Them Apart?  
<div style="width:100%;text-align:center;">
<table>
<tr>
  <td>  <a href="images\01_5VPCB.jpg" data-lity>
    <img src="images\01_5VPCB.jpg" style="width:400px; border:2px solid CornflowerBlue">
  </a>
  </td>
  <td>
    <a href="images\01_24VPCB.jpg" data-lity>
    <img src="images\01_24VPCB.jpg" style="width:400px; border:2px solid CornflowerBlue">
  </a>
  </td>
</tr>
<tr>
  <td>5V Version</td>
  <td>24V Version</td>
</tr>
<tr>
  <td>Note the absence of 24V markings<P>  
      Note the size and orientation of SMT components</p></td>
  <td>Note the 24V markings on the PCB<P>  
      Note the size and orientation of SMT components</p></td>
</tr>
<tr>
  <td><span style="color:blue">Click images to enlarge</span>
  </td>
  <td><span style="color:blue">Click images to enlarge</span>
  </td>
</tr>
</table>
</div>  

{% include tip.html content="The 24V version will ALSO work connected to 3.3V/5V endstop ports on the same controllers. However, the LED's might be a little dim in comparison. " %}  

### How does it Work?  
Very well actually.... here are some photos of the toolboards with 3.3V, 5V and 24V running through them. As you can see, the 3.3V is slightly dimmer than the 24V, but still bright enough to see.  

<div style="width:100%;text-align: center;align-items: center">
<table>
<tr>
   <td> <a href="images\01_assembly\3.3V.jpg" data-lity>
   <img src="images\01_assembly\3.3V.jpg" style="width:250px; border:2px solid CornflowerBlue"></a>
   </td>
   <td> <a href="images\01_assembly\5V.jpg" data-lity>
   <img src="images\01_assembly\5V.jpg" style="width:250px; border:2px solid CornflowerBlue"></a>
   </td>
   <td> <a href="images\01_assembly\24V.jpg" data-lity>
   <img src="images\01_assembly\24V.jpg" style="width:250px; border:2px solid CornflowerBlue"></a>
   </td>
</tr>
<tr>
   <td style="width:300px"><span style="width: 100%;text-align: center;align-items: center">24V Euclid Probe Prototype on 3.3V</span></td>
   <td style="width:300px"><span style="width: 100%;text-align: center;align-items: center">24V Euclid Probe Prototype on 5V</span></td>
   <td style="width:300px"><span style="width: 100%;text-align: center;align-items: center">24V Euclid Probe Prototype on 24V</span></td>
</tr>
</table>
</div>
If you want to see how the circuit works, the Falstad.com simulations are linked below. Click on the swtich to see the Z_Probe pin input change. 
<div style="width:100%;text-align: center;align-items: center">
<table>
<tr>
  <td>
    <a href="https://tinyurl.com/yawtohnf" data-lity>
    <img src="images\00-falstad.jpg" style="width:400px; border:2px solid CornflowerBlue"></a>
  </td>
  <td>
    <a href="https://tinyurl.com/y9l7q26f" data-lity>
    <img src="images\00-falstad.jpg" style="width:400px; border:2px solid CornflowerBlue"></a>
  </td>    
</tr>
<tr>
  <td>Euclid as typical 3.3V/5V endstop or Z-Probe input simulation<p>
  <span style="color:blue">Click images to enlarge and simulate</span></p></td>
  <td>Euclid as 24V Z-Probe input simulation<p>
  <span style="color:blue">Click images to enlarge and simulate</span></p></td>
</tr>
</table>
</div>

###  Logic Voltages  
Generally speaking, 16bit boards used 5V logic and 32bit boards used 3.3V logic. Example 16bit controllers include MEGA/RAMPS. AM based Duet3d controllers, LPC based controllers like Smoothieboard, SKR1.4, MKS Base, etc... All Euclid Probe versions will work with these controllers when plugged into a normal endstop port.  

The 24V capable PROBE ports on the various controllers are not standard or uniform. While we do our best to try and provide users all the necessary documentation as we encounter the various controllers.  Users should expect to coordinate the wiring of Euclid Probe to their controller and their firmware configuration.  

As always, if you need assistance or have questions, please feel free to contact us via the Feedback link above of via the Discord channel.  

