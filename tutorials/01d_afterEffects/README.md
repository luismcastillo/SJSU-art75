
# After Effects


 ◇─◇──◇────◇────◇────◇────◇────◇─◇─◇
<br />


#### On this page:

1. Keyboard Shortcuts
2. Tutorials
3. How to export
4. Tips on working between Adobe App

<br />

## ▼△▼△▼ Keyboard Shortcuts

|                                 |                                                                                            |
|---------------------------------|--------------------------------------------------------------------------------------------|
| ***Timeline Panel Shortcuts***                  |                                                                                            |
| I / O                           | Move cursor to in/out point of layer                                                       |
| home / end                      | Move cursor to beginning/end of composition                                                |
| cmmd right/left arrow           | Move cursor to left or right by one frame                                                  |
| Shift page up / shift page down | Move cursor to left or right by 10 frames                                                  |
| Enter timecode                  | You can also move cursor to specific frame by typing in the timecode in the left top field |
| [ / ]                           | Slides layer in/out to cursor                                                              |
| opt [ / opt ]                   | Slips layer in/out to cursor                                                               |
| J/ K                            | Previous/next keyframe                                                                     |
| B / N                           | Set work area start / end                                                                  |
| U                               | Reveals all animated properties of a layer                                                 |
| UU                              | Reveals all the properties you changed.                                                    |


|                    |                                                 |
|--------------------|-------------------------------------------------|
| ***Tool Shortcuts***     |                                                 |
| V                  | Selection tool (arrow)                          |
| H                  | Hand tool                                       |
| spacebar           | Temporarily activate Hand toll                  |
| Z                  | Zoom in tool                                    |
| Option (with zoom) | Zoom out (when zoom already activated)          |
| Y                  | Pan-Behind Tool                                 |
| Q                  | Activate and cycle through mask and shape tools |
| Cmmd  T            | Type Tool                                       |
| G                  | Pen Tool                                        |

---

## ▼△▼△▼ Tutorials

***Lynda Tuts***
* The Lynda tutorial ***[After Effects CC 2018: Essential Training](https://www.lynda.com/After-Effects-tutorials/After-Effects-CC-2018-Essential-Training-Basics/651227-2.html)*** is a quick and dirty introduction to the interface.
* Also on Lynda, ***[After Effects Apprentice](https://www.lynda.com/After-Effects-CS5-tutorials/apprentice-series-basic-animation/78544-2.html?srchtrk=index%3a9%0alinktypeid%3a2%0aq%3aafter+effects+apprentice%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2)*** is an excellent, comprehensive tutorial series on Lynda.

<br />
<br />

***Adobe Support Docs***
* [On masking and rotoscoping](https://helpx.adobe.com/after-effects/using/animating-shape-paths-masks.html)
* [Dynamic link between After Effects and Premiere](https://helpx.adobe.com/premiere-pro/using/dynamic-link.html)

***Youtube Tutorials:***
* [Keyframing movement](https://www.youtube.com/watch?v=u5YxwHkjMHc)
* [Different types of keyframes ](https://www.youtube.com/watch?v=t5rOILpSqcM) (Includes linear, roving, easy ease and hold keyframes)
* [Using the Rotobrush](https://www.youtube.com/watch?v=EoQLE57XzT0)
* [Using Keylight to work with green-screen footage](https://www.youtube.com/watch?v=5dbr105_gSs)
* [Isolating and changing a color in your scene](https://www.youtube.com/watch?v=PtVo6XwA13A)
* [Animating a mask in an adjustment layer](https://www.youtube.com/watch?v=StCBpTIwOFE) (Decent tutorial but I recommend feathering the mask a little more)
<br />
<br />

---

## ▼△▼△▼ EXPORTING

Step-by-step tutorial on exporting.

![Add to Render Que](assets/AE_exporting_01.png)

![Set destination and open up codec menu](assets/AE_exporting_02.png)

![Open up quicktime format options menu](assets/AE_exporting_03.png)

![Select H264 codec](assets/AE_exporting_04.png)

![Click to render](assets/AE_exporting_05.png)

---

## ▼△▼△▼ Tips for Workflow between Adobe Apps

**Importing Photoshop and Illustrator files into After Effects.**
  * Make sure you select "Composition - Retain Layer Sizes" in import dialogue. This will preserve Photoshop layers. If default "Footage" is selected, you will get one flat image

![Import Dialogue](assets/AE_importPhotoshop+IllustratorFiles.png)

<br />

**Workflow between After Effects and Premiere.**

Adobe Dynamic Link

Dynamic Link allows you to import *live* sequences from Premiere into After Effects, or *live* comps from AE into Premiere, so the items auto-update as you change files in either program.

Limitations:
* You can only go in one direction via Dynamic Link, you can't have AE linking to Premiere AND Premiere linking to AE in the same project.
* You can't see layers/tracks on the imported items.

So Dynamic Link works well for **AE --> Premiere workflow,** overlaying After Effects animation on Premiere sequences.

BUT if you want to go from **Premiere --> After Effects,** Dynamic Link will flatten Premiere sequences as a single track.

If you want to preserve Premiere video tracks in After Effects, you have to import a *static* Premiere Project, NOT using Dynamic Link. This means it won't update, so only move from Premiere to AE once your edits are locked.

So the two different ways of importing Premiere into After Effects:

1. Using Dynamic Link

![Using Dynamic Link](assets/AE_DynamicLinkPremiere.png)

2. Importing a static Premiere Project

![Import a Premiere Project](assets/AE_ImportPremiereProj.png)

<br />
<br />
