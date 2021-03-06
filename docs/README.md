# Fit-To

*A library that allows developers to customize the layout of their page*
## Description
Fit-To
Particularly useful for photography,journalism and news blogs as they can personalize the layout of their content and see what potential layouts will look like. With the abilities, to drag to different parts of the page, resize content and temporarily hide sections. Content such as images or tables, automatically resize to fit the containers they've been dropped in and developers can also use the content bar feature which stores all content in one area.

This is simplified way to visualize what layout you can possibly choose.

# Getting Started
>Files to include 
- Include library file          
        <script  src = "js/Library.js" charset = "utf-8"></script>

- Include CSS file 
        <link rel = "stylesheet" href = "style.css">

- Jquery
        <script src = "https://code.jquery.com/jquery-1.10.2.js"><script>

## Creating Objects 
        const newObject = new myLibrary({
            
            //Must pass in id of element 
            selectors: ['#id1',#id2],
         
            //Must pass in id of element
            id: ['#image1,'#table2']
        })

        //Can now access methods
        newObject.resize()

 ### Notes:  
 - The id field is for content such as images or tables that will be dropped into containers 
 - The selctor field is for elements that the user wants to resize, drag and accept droppables

## Methods and Arguments 
A list of all methods and their arguments 

        //Drag elements
        myLibrary.drag()
       
        //Resize elements
        myLibrary.resize()
       
        //Hide an element temporarily 
        myLibrary.hidden({selector: ['#box']})
       
        //Place content in a 
        myLibrary.contentBar({
            id: ['#image2',#image3'].
            elementToAppendTo: '#box'
             minWidth: 200,  
             minHeight:200,
             width: 200,
             height: 300
        })
#### Drag 
        //Drag elements
        myLibrary.drag()

No paramaters are passed for this method. Drag an element from its center.

#### Resize
        //Resize elements
        myLibrary.resize()

Resizes elements in the South-East, South-West, North- West and North-East corners. Hovering over those areas, the cursor to resize will appear.
#### Hidden
        //Hide an element temporarily 
        myLibrary.hidden({selector: ['#box']})
This method take an array of id's as an argument 

#### Content Bar
         myLibrary.contentBar({
            id: ['#image2',#image3'].
            elementToAppendTo: '#box'
             minWidth: 200,  
             minHeight:200,
             width: 200,
             height: 300
        })
- This method takes an array of id's as an argument. The id's are for the content. 
- elementToAppendTo: pass in the id of the element you want to append the content bar to
- minWidth and minHeight are the dimensions of the container for the content. The container however, increases to fit the size of its contents. 
- width & height, are the dimensions of the content being placed into the container

