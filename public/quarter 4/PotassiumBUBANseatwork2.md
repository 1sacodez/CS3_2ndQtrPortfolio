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
  <meta name="author" content="BELLA, Balingit / ISA, Buban" />
  <meta name="revised" content="March 27, 2026" />
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

- Answer: The green container with the text "Sidebar" was moved 20px farther from the bottom of the header, and the left, moving it relative to its default, static position. 

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

- Answer: When you scroll the page, the blue footer stays in place-- at the bottom of the viewport, with no space between it and the very bottom. This is because of the "fixed" position in its styling. It also stretches to cover the entire width of the screen because of the "100%" width.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

- position: absolute moves an element relative to its nearest positioned ancestor (an ancestor element with position: in its styling). In this case, that ancestor element is the sidebar, which is why the content box is found beside it. Meanwhile, fixed moves it relative to the viewport.

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

- Answer: z-index controls the vertical stacking order of positioned elements that overlap. In this case, notice appears on top of content because higher z-index values appear on top. If you switch the values, content will be the one on top.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?
sir i'd love to answer this but i kinda have uhhhhhh 12 MINUTES AND A MATH EQE TO STUDY FOR AFTER THIS !!@!@!@!!

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 
      STATIC: default positioning, elements appear according to their order in the document
      RELATIVE: relative to its normal position
      ABSOLUTE: relative to its nearest positioned ancestor
      FIXED: relative to viewport, element stays in place while scrolling

    b. How does absolute positioning depend on its parent element?
      Absolute positioned elements are positioned relative to the parent positioned element.

    c. How do you differentiate sticky from fixed (you can research on sticky)?
      Sticky allows the element to move while scrolling, acting like relative positioning, before it becomes fixed at a certain, specified point.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
      - Webpage headers and footers being fixed at the top and bottom provide easier navigation between pages for the viewer
      - Lots of information and containers may need to be cramped in one place on the webpage. z-index allows the user to control what information may be prioritized and placed on top.