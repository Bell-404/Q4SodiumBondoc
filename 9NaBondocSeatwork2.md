# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    b. How does absolute positioning depend on its parent element?

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    ### Answers:
    ##### Guided Questions
    1. The sidebar moved the given amount of px from its default static positioning.
    2. The footer stays in place on the screen when scrolling through the page, compared to the sidebar with position relative, which moves along with the scrolling page.
    3. Absolute makes the position of the element relative to its nearest positioned ancestor. Meanwhile, the fixed position is relative to the viewport/screen.
    4. The notice appears on top of content because of the z-index, which indicates the positioning of elements from back (1) to front. If you swap the index values, .notice will appear behind .content/their positions will swap.

    ##### Challenge
    1. ![My Photo](SW2 Image.HEIC)
    2. Relative : .content becomes 66px above and 200 px to the right of its default static positon.
       Fixed : .content is still at the same position as it was with absolute, it stays in place on the viewport when scrolling.
    3. An element with a higher z-index will be in front of elements with lower z-index.

    ##### Reflection
    a. static - default positioning, element is placed normally on the document flow.
    relative - element is positioned relative to its static positioning.
    absolute - element is positioned relative to its nearest positioned ancestor.
    fixed - element is positioned relative to the viewport, it stays in place even when scrolling.

    b. Absolute positoning depends on the parent element's position in the webpage. It starts on the top left corner of the parent element then moves according its placement (top, bottom, left, right).

    c. Sticky positioning first lets the element to scroll along with the webpage like a static element (unlike the viewport element that stays in place the whole time when scrolling), then it acts like a fixed element once it reaches its proper position on the viewport.

    d. If I were designing a webpage for a school event, I would mainly use fixed, sticky, and z-index positioning for highlighting important information.

    Fixed positioning would be used for important icons and elements that have to be easily accessed anywhere you scroll on the webpage such as sidebars, headers, previous, exit, and next buttons.

    Sticky positioning can be used for important details mentioned in the webpage documents that can stay in place when not yet seen, but follow along on the viewport as the user scrolls.

    Z-index would be used for reminders, notices, and anything else that the user must see first on screen.
