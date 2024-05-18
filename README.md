# DJS04 Project Brief: Book Connect - Web Components
For this project we are building upon the "Book Connect" in DJS03, we dive into Web Components. This challenge will refine our skills in creating reusable, encapsulated and interactive elements.


![alt text](image.png)

# Project Overview
#### Goals
* Convert Book Preview to Web Compoonent: The main focus is to encapsulate the book preview feature into a Web Component, making it reusable and independent.
* Assess Other Components: Identify other elements within the "Book Connect" app that could benefit from being converted into Web Components.
* Maintain FUnctionality: Ensure that the application retains all its current functonalities after refactoring.


# Project Process
* After getting the starter code from my DJS03 project which I had worked on. I started by analyzing the styling sheet to see which styles I can use for my web components.
* I then created new custom element class that extends the buil-in HTMLElement.
* I then created a constructor method which inside it had the super() which calls the constructor of the parent HTMLElement class,I then attached a shadow DOM tree to the custom element using attachShadow method.
* I then created a template element which I then added innerHTML to it which I add the style and the button and it's inner elements which I had previously used inside the function createBookElement.I then cloned the template content and appended it to the shadow DOM.
* I then addeed a connectedCallback which is a method called when the custom element is added to the DOM which then inside it I assigned the shadow root of the custom element to a variable wich I used to set the source attribute of the image element, set the text of the title element and inner text set attribute which will all be used in the createBookElement to set image, title, author and id using the getAttribute.
* I then used customElements.define which registers the custom element  with the browser, making it availabe in the DOM as "book-preview".
* I then access the book-preview custom element in the createBookElement function by using createElement which I just add 'book-preview' in it and used the setAttribute to assign the destructured variable to the right attribute.
  

# Challenges
The one problem I had was trying to create web components for creating option elements for search form to get the genre and author to be rendered. I have tried many solutions and nothing seems to work, the element select does get the option elements but seems to not render properly, so I ended up not making it a web component.

# Feedback
This has been one of the few challenging projects since starting the course, the material provided confused me even more. I got help by doing more research on the side and using youtube.
