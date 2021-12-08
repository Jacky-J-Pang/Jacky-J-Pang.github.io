---
layout: essay
type: essay
title: Assignment 3 Chck PT
date: 2021-12-07
labels:
  - Software Engineering
  - Learning
  - CheckPT
---
1.	Show what each page will look like. The pages do not have to be “functional” but the design should clear. Here is an example PPT prototype
    See attacehd PPT in Laulima 
    
2.	Describe your design for your site’s shopping cart. That is, will it be a separate page that the user can view and edit, or will it be integrated into the product pages? If so, describe in detail how this will work on your site. Provide several examples of using the cart.
  
  For assignemtn 3 I am goining to do a compelete revamp of the entire project (old code was meh). For the products dispaly page I am planning to having the options to add your products to your shopping card and can be used via session ID. The property of the shopping card is the similar to a invoice file but still the user still have the option to change the quantity before the "actual Invoice" shows up. 
    
    
3.	Explain specifically how you will use sessions to manage your shopping cart. In particular, what shopping cart data will be stored in the session, what data format will be used (NOT what data type, but the format like with the data format used for your registration data). Use code examples showing what data structures (such as arrays and their objects) you will use to manage the shopping cart data and how they will be used in a session.
  
  Proabbly some validations to check sessionID and .get the necessary array format and establishing data structures. Shopping cart data will just consist of user data, but upon checking out the process to take yourself to invoice. It verifies if stock is enough again, to makes sure other useres do not use the same session. Also the online inventory will only update after invoice is generated to ensure the inventory is the up to date and not stalled because someone has it in their shopping cart. to behonest Im not very sure on how the best use of data format to be. Was thinking SQL but still not sure what to with it. 


4.	How will you avoid access to your application when the user has not logged in or registered? What are the particular security concerns you must address?
 
 Security concerns such as encrypting the cookies session to not have a unauthorized user to use the cookie and login.  To prevent users from getting to different pages 
 such as acessing the inovice session I will use the following validation statement as such transfer them back to the orignial file and make them take again with a data validation object
     
     if(params.has('username')){
    }
    else{ //if the invoice page doesn't recieve username info,  send back to product display
      alert('Please login before checkout');
      window.location = 'login.html';
      window.stop();
    }
    if (params.has(`purchase_submit`)) 
    {} 
    else{
      alert('You must enter the amount of wallpapers you want to purchase');
      window.location = 'products_display.html';
      window.stop();}
    
    
5.	Upon a successful login, how do you provide personalization in your UI? Explain how you did or will do this (paste code if necessary)
     
   <h1> <script>document.write(`Thank you for your purchase ${params.get('username')}!!!`);</script> </h1> and paste it in the code and have a if statement validation when        equals to udnefine hide the content. 
    use params.get function 
    whereas function equals to (new URL(document.location)).searchParams;
    
    
6.	If you are working with partners, how will you split up the work in your team so that you are working in parallel as effectively as possible? That is, who is doing what and when?
N/A
