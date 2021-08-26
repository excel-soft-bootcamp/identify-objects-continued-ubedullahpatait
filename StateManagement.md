 StateManagement
      
      Client-side Management                                  
     The client side state Management its store the information in client side its communicate with server side when we send request to server
     afterward reponse the server side
     its store the data on client side


     Server-side Management
     The server side state management its doing some operation and functionality whatever come from client side



    client side techniques
    
    1)view 
    2)hidden
    3)cookies
    4)control state
    5)query string
    
    
    1)view
    its use for storing data in in asp.net apllication want to store data temporary.
    its store any type of data
    This property is enabled by default but we can make changes depending on our functionality, 
    what we need to do is just change the EnableViewState value to either TRUE for enabling it or FALSE for the opposite operation.
    
    It is page-level State Management
    Used for holding data temporarily
    Can store any type of data
    Property dependent
    
    2)Hidden
    a hidden field is used for storing small amounts of data on the client side
    it just contain object but its result not visible on web browser
     contain small amout of memory
     Direct functionality access
    
    3)cookies
    a set of Cookies is a small text file that is stored in the users hard drive using the client's browser.
    it only stores information such as sessions id 
    whenever we connect to internet to the internet for accessing a specific service
    the cookie file access from hard drive via our browser for identify the user
    
    Store information temporarily
    It's just a simple small sized text file
    Can be changed depending on requirements
    User Preferred
    Requires only a few bytes or KBs of space for creating cookies
    
    4)control state
    used to enable the state property
    define custom view
    Used for enabling the View State Property
    Defines a custom view
    View State property declaration
    Can't be modified
    Accessed directly or disabled
    
    
    5)Query String
     its used for holding some value from a different page and move these values to the different page
     It is generally used for holding values
     Works temporarily
     Switches info from one to another page
     Increase performance
     Uses real and virtual path values for URL routing
    
    
    server side technique
    1)Session State
    2)Application State
    
    1)Session State
     Basically session is variable it use between client and server that is store on the server side
     its store either internet information service or Sql server information
     so a session helps to maintain the user state and data all over the application by storing the information on the server memory
     session can store any kind of information.
     
     2)Application State
     application State is stored in the memory of the the server and is faster than storing and retrieving information in a database.
     Application State does not have a default expiration period.
     when we close the work process the application object will be lost.
    it store value in key and value pair
