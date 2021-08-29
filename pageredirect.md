# PageRedirect

**Response.Redirect**

Response.Redirect are used to transfer a user form One page to another web page.
- In this transfer is done by browser
- When we navigate Browser URL changes to redirected target page
- We can navigate any site or any page whether 
  They are present on same web server or different web server
- When we navigate Browser URL changes to redirected target page
  

Ex:
```C#
protected void Button1_Click(object sender, EventArgs e)
 {
    Response.Redirect("WebForm2.aspx");
}
```


![responseredirect1](https://user-images.githubusercontent.com/67995958/131157294-4e6cd86e-b05b-4d78-86c3-1e903b8224b8.png)

if you want to intercept a click event in code use Button.In the button click event call Response.Redirect() method.
when the user click the button, the web server recieves, a request for redirection.The server then sends a response header
to the client. The client then automatically issues a  new GET request to the web server. The web server send the another
page to browser.

 **Server.Transfer**
 - Done by server
- Browser Url doesn't change
- when we need  to redirect between pages of
  the same server
- Server.Transfer allows only relative URL<br/>


  Ex:
```C#
  protected void Button1_Click(object sender, EventArgs e)<
 {
    Server.Transfer("WebForm2.aspx");</br>
}
```

![2](https://user-images.githubusercontent.com/67995958/131208431-0ab04080-fa36-4482-b7a5-eb3a1ad0c955.PNG)

**Server.Execute**
- Server.Execute is used to begin excuting a new webform while still displaying the current web Form

Ex:
protected void Button1_Click(object sender, EventArgs e)
 {
    Server.Execute("WebForm2.aspx");</br>
}


**HyperLink**

- it is control that is used to create a  hyperlink. it responds to click event.
- we can use it to refer any page on the server.
Ex:
 ```C#
   <asp:HyperLink ID="HyperLink1" runat="server" NavigateUrl="~/WebForm2.aspx">HyperLink</asp:HyperLink>
```
**Cross Page Posting**
- The cross page posting technique allows a web form to post on another web form on button click
- The Postback property of the button is set to the page where you want to do cross page posting

Ex:
```C#
- source.aspx

<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox><br>
   
<asp:Button ID="Button1" runat="server" Text="submit" PostBackUrl="~/Destination.aspx" /><br>

- Destination.aspx

            Page previousPage = Page.PreviousPage;<br>
            if (previousPage != null && PreviousPage.IsCrossPagePostBack)
            {
                Label1.Text = ((TextBox)previousPage.FindControl("TextBox1")).Text;<br>
                Label2.Text = ((TextBox)previousPage.FindControl("TextBox2")).Text;<br>
            }
```            
   

