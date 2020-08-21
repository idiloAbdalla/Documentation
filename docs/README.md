# Fit-To

*A library that allows developers to customize the layout of their page*
## Description
Fit-To
Particularly useful for photography,journalism, news blogs as they can personalize the layout of their content and see what potential layouts will look like. With the abilities, to drag to different parts of the page, resize content and temporarily hide sections. 

# Getting Started
>Files to include 
- Include library file          
        <script  src = "js/Library.js" charset = "utf-8"></script>

- Include CSS file 
        <link rel = "stylesheet" href = "style.css">

- Jquery
        <script src = "https://code.jquery.com/jquery-1.10.2.js"><script>


## Example

- Use code snippet, showing what it would look like 

# API Calls 

## Creating Objects 
        const newObject = new myLibrary({
            
            //Must pass in id of element 
            selectors: ['#id1',#id2],
         
            //Must pass in id of element
            id: ['#image1,'#table2']
        })
 ### Notes:  
 - The id field is for content such as images or tables that will be dropped into containers 
 - The selctor field is for elements that the user wants to resize, drag and accept droppables

## Methods and Arguments 
        //Drag elements whose id's were
        myLibrary.drag()
       
        //Resize elements
        myLibrary.resize()
       
        //Hide an element temporarily 
        myLibrary.hide()
       
        //Place content in a 
        myLibrary.contentBar({
            id: ['#image2',#image3'].
            elementToAppendTo: '#div2'
             minWidth: 200,
             minHeight:200,
             width: 200,
             height: 300
        })

### Note: 
- elementToAppendTo takes id's as argument 
- minWidth & minHeight are the dimensions of the container for the content
- width & height, are the dimensions of the content being placed into the container

