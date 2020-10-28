# Mug Shots

## A Code Institute Milestone 4 Project
Live Demo: (https://mug-shots.herokuapp.com/)

The Mug Shots e-commerce website is developed for a fictional handmade pottery company who specializes in custom mugs. 
The main idea for this project was to combine all of the content learned from the Full Stack Developer course. 
This website is made with Django to build a fully functioning e-commerce website. 

If you would like to test the payment functionality of this project, please use the following payment details:
- Card number: 4242 4242 4242 4242 
- CVC: any 3 digit number
- Exparation Date: any future date
- Address: any address details

The app is deployed on Heroku. 
Click here to view the deployed site

# Table of Contents
1. [UX](#UX)
    - [Main Requirements](#Main_Requirements)
    - [User Stories](#User_Stories)
    - [Design](#Design)
    - [Wireframes](#Wireframes)
    - [Database Structure](#Database_Structure)
2. [Features](#Features)
    - [Existing Features](#Existing_Features)
    - [Features Left To Implement](#Features_Left_To_Implement)
3. [Technologies](#Technologies)
4. [Testing](#Testing)
5. [Deployment](#Deployment)
    - [Local Deployment](#Local_Deployment)
    - [Heroku](#Heroku)
6. [Acknowledgement](#Acknowledgement)
7. [Credits](#Credits)


## UX

### Main Requirements
The Main requirement of this project was to create a full stack e-commerce website where both the user is able to 
successfully purchase a product and the owner is able to satisfy all CRUD functions to Create, Read, Update, and 
Delete products and reviews.

#### Additional requirements
* To view all products in a list
* View products individually with detailed product information
* Purchase the products using a secure checkout system
* Create an account, view/update personal information and view previous orders
* Contact the business for further information and technical support

#### Expectations
* Website is visually appealing and easy to navigate on all devices
* User can leave a review of the business and/or product
* User can edit their reviews
* Personal information will be stored securely, but will be able to be accessed when logged in


### User Stories
| User Story ID                  | As a/an     | I want to be able to…                                             | So that I can…                                                                |
|--------------------------------|-------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Viewing and Navigation         |             |                                                                   |                                                                               |
| 1                              | Shopper     | View a list of products                                           | Choose one to purchase                                                        |
| 2                              | Shopper     | View product details                                              | Identify price, description, and image                                        |
| 3                              | Shopper     | View the cart at anytime                                          | To manage my purchase                                                         |
| 4                              | Shopper     | Adjust the quantity of items in my cart or completely remove them | To manage my purchase                                                         |
| Registration and User Accounts |             |                                                                   |                                                                               |
| 5                              | Site User   | Register for an account                                           | Have a personal account to view my profile                                    |
| 6                              | Site User   | Login and Logout                                                  | Easily access my personal information                                         |
| 7                              | Site User   | Recover my password                                               | Recover access to my account                                                  |
| 8                              | Site User   | Receive an email conformation                                     | Verify my registration was successful                                         |
| 9                              | Site User   | Have a personalized user profile                                  | To view my personal information such as payment information and order history |
| 10                             | Customer    | Leave a review                                                    | Leave my testimonial and support this small business                          |
| 11                             | Customer    | Edit my review                                                    | Edit my previously created review with new details                            |
| Sorting and searching          |             |                                                                   |                                                                               |
| 12                             | Shopper     | Sort the list of products                                         | View the available products by the size I prefer                              |
| 13                             | Shopper     | Search for a product by name or description                       | Quickly find the product I am interested in                                   |
| Purchasing and Checkout        |             |                                                                   |                                                                               |
| 14                             | Customer    | View items in my bag to be purchased                              | Identify the products and total cost before I purchase                        |
| 15                             | Customer    | Adjust the quantity or remove items in my bag                     | Easily make changes before checkout                                           |
| 16                             | Customer    | Enter my payment information                                      | Check out easily with no problems                                             |
| 17                             | Customer    | View an order confirmation after checkout                         | Verify there are no mistakes with my address, order, or payment information   |
| Admin and store management     |             |                                                                   |                                                                               |
| 18                             | Store Owner | Add a product                                                     | Add a new item to my store                                                    |
| 19                             | Store Owner | Edit a Product                                                    | Change any details in the price or description                                |
| 20                             | Store Owner | Delete a Product                                                  | Remove items that are no longer available                                     |
| 21                             | Store Owner | Edit and Delete reviews                                           | To be able to manage customer reviews                                         |

### Design

Doing some research on popular e-commerce websites, I was able to form an idea of how I wanted the atmosphere of the website to look. I knew that as a user of the website it would be important to have a simple design. Through my research, I found some websites that I thought were 
messy in their layout and hard to navigate. I knew I wanted my website to be image-led and very minimalistic with easy navigation.

With the basic idea in place, I knew the features of the website must be divided between three categories: 1) external users (anonymous users, who are not yet authenticated), 2) users who are logged in to their accounts, and 3) the store owner (also known as the superuser). All users are able to 
view the products in the store and the reviews in the gallery page. Only users who are logged in will be able to view their past order history, personal billing information, and edit or delete a review they previously created. The site owner would be able to view everything the users can view but 
will also be able to add, edit, and delete products from the store as well as manage the reviews. With this in mind, I decided on adding these feature ideas when creating my wireframes: 
* login/registration system 
* ability to leave reviews
* a gallery containing photos
* the ability to add desired products to a cart 
* confirm the purchase with a payment through Stripe
* ability to contact the store owner with any questions
In order to keep the user informed throughout their experience on the website, I also decided to add a notification system using Bootstrap's toasts feature, confirming the actions a user would take. For example, deleting a product from their cart or adjusting the quantity. 
The website also must meet content requirements to provide users with enough information about each product, including item pricing and details.

For this project, I chose a minimalistic dark mode style website. To soften the styling as to not have a harsh black or white, the colors #161616 (Muted black) and #dfdfdf (A light Gray, white color) were chosen for the main colors of the site.
These colors make up most of the website with two additional colors to help certain elements such as the buttons and titles pop. The colors, #d4af37 (Gold) and #133616 (Forest Green) were chosen to complement the main black and white design. 

For the font, I chose the classic font, "Ubuntu" for the main text on the site. This font is very clean to read and works well with the minimalistic theme. I wanted an additional font to make some of the titles and buttons stand out, so the font "Ranchers"
was chosen. The Ranchers font is bold, but still very clear and easy to read, giving the site a nice finishing touch.

The navigation bar was originally designed in the wireframes to display the logo of the site above the navigation bar. After working on the development of the site, it seemed to be more practical to have all of the navbar contents on the same line.
This helped to keep to a more minimalistic design. A feature was added where the navbar is transparent when the page is first loaded, but changes to the light gray color (#dfdfdf) on scroll. On large and medium screens, the user will be able to see which page
they are actively on by the white shadow you can see on the coffee cup icon.

Keeping to the minimalistic design, all of the forms have simple pages. The login/registration process contains only a form that will accomplish the specific action, such ad logging in, signing up, confirming email, and so on. The contact form on the contact
page follows this same design as well as the reviews form located on the contact page. To style the forms, I used the css property of box-shadow to create shadows & highlights underneath the forms giving it a slight glow. This css property uses horizontal & vertical offsetting
along with blur and spread and finally the color of the shadow itself to produce the desired effect.

A note about the 'cart' application. In the beginning, the site was developed using the term 'bag' as reflected in the code. However, it came to my attention that the users in the area where this website would be used, prefer to say 'cart' when shopping online. 
Thus, on the front end of the website, the term 'cart' is used instead of 'bag'.

###### Defensive Design

Throughout the build of this site various defensive features were added to protect against malicious activity, and also to stop things breaking.

A {% csrf_token %} was added on every form to prevent Cross Site Request Forgeries.

Included in a lot of the views and a lot of the templates are checks to ensure that the user has been authenticated. This helps avoid somebody who is already logged in to log in. It also helps ensure only registered users are accessing certain functions, such as making and editing reviews or viewing a personalized profile.

Several checks were put in place within the forms and the models to ensure all requests were receiving all the expected data. Adding 'required' to certain field helped ensure this was achieved and fields were not left blank.

The Google Chrome's Dev Tools were used to view the results of new features added on different screen sizes. Doing so helped me make any adjustments to styling including; the margins, padding and font sizes of different aspects of the project, as well as checking that new features were compatible on all screens. The functionality of each feature was tested as it was added to the project to notice issues as they arose.

### Wireframes
> Home Page
![Home](wireframes/home.png)
![Home Mobile](wireframes/mobile-home.png)

> Shop Page 
![Shop](wireframes/shop.png)
![Shop Mobile](wireframes/mobile-shop.png)

> One Product Page 
![One Product](wireframes/oneproduct.png)
![One Product Mobile](wireframes/mobile-oneproduct.png)

> Gallery Page
![Gallery](wireframes/gallery.png)
![Gallery Mobile](wireframes/mobile-gallery.png)

> Contact Page
![Contact](wireframes/contact.png)
![Contact Mobile](wireframes/mobile-contact.png)

> Cart Page
![Cart](wireframes/cart.png)
![Cart Mobile](wireframes/mobile-cart.png)

> Checkout Page
![Checkout](wireframes/checkout.png)
![Checkout Mobile](wireframes/mobile-checkout.png)

> Login/Register Page
![Login/Register](wireframes/login.png)
![Login/Register Mobile](wireframes/mobile-login.png)

> Profile Page
![Profile](wireframes/profile.png)
![Profile Mobile](wireframes/mobile-profile.png)


### Database Structure
During development with Django, I used the SQLite3 database. After the project was deployed to Heroku, 
I changed to using a PostgresSQL database that is provided by Heroku as an add-on for production. 
I also relied on Django’s default user model for authorization, allowing me to meet one of the project requirements of separating features by anonymous users, users in session, and superusers. 
The structure of the Checkout and Services apps were inspired by my studies with Code Institute, namely the Boutique Ado project. 

The Database Structure was first drawn to see how the database data would relate to each other across the site.
{{{ Handrawn picture}}}

After the rough sketch was drawn, I was able to use Numbers (Apple's built in spreadsheet software) to help plan the structure of the models.

When each app and its models were created and implemented, python manage.py makemigrations was run in the terminal to create the initial model package and python manage.py migrate was then used to apply the model to the database and create the table.

{{{Models}}}

Whenever possible, first-time-right methodology was used when creating each of the models to avoid too many alterations to the models and the database table through multiple makemigrations and migrate commands. 
Throughout development, a few of the fields were adjusted and those commands needed to be run again.


## Features
### Existing Features

This project is fully responsive and renders as expected on all up to date browsers. It also contains several pages many key features.

##### Navbar
All pages contain a navigation bar to allow for easy access. 
The menu at the top of the page is consistent in design and are responsive throughout the website. 
It contains links to the main pages for the site to allow for easy access. 
However, the contents of the menu changes depending on if a user is logged in or not.
The navigation bar for logged in users features a 'Logout' link where the 'Register' and 'Login' links usually are. 
When a user in session chooses to sign out, a message confirms this action and they are redirected back to the home page.
The active page is highlighted in a light gray color to show the user which page they are on.

##### Footer
The Footer at the bottom of the page is consistent in design and is able to be viewed across the site.
This section of the page contains contact information, links to the store social media, and a search bar to allow the user to search for products in the store.
If no products are found or the search bar is submitted blank, a message will appear inviting the user to try again.

##### Home page
The home page is the main landing page for this site. It features a large image with a call to action button to begin shopping.
The user is also able to see a short paragraph and photo in the about us section about the company.
There is also a small responsive grid of photos that will allow the user to visit the company instagram to view more photos. There is 
another call to action button at the bottom of the page to invite the user to purchase a product.

##### Shop page
The shop page contains all products in database in a card, designed to look like a Polaroid. Each card contains the product image, name, price, category, and a button to view more details.
Bootstrap's grid helps the cards to display in a responsive way.
At the top of the page, the user is able to view the available products by category and sort all products by price or size.

##### One Product Page
The One Product Page displays aditional information about the selected product from the shop page. The user will be able to view the name, price, category, description, and sku.
There is a quantity box to allow the user to add any number of the selected product to the cart.
A product can be added to the cart by clicking the button at the bottom of the page "Add to Cart". If the item is successfully added to the cart, the grand total price in the navbar will increase
and a toast message sucess will show the current contents of the cart. 
If the user is admin, there are also 2 buttons displayed in the cards: Edit and Delete. Clicking Edit button redirects admin to the Edit Product page. 
Clicking the Delete button deletes the product. The page reloads and the toast message will inform about the successful deletion. 
These actions can be done only by superuser, attempts to access them by other users will end up redirected to the homepage with toast error messages displayed.

##### Gallery page
The gallery page was created to showcase the potential products that can be viewed in the store. The responsive grid located at the top of the page contains many images. When hovering over the images, 
the name of the product and number of hearts can be seen. Clicking on any of these images will take the user to the store's instagram page.
Below the image grid are the review cards. Any user can view the previously created reviews. They are stored in the database with the fields: title, author, message, and product name. 
If a user is logged in, they will be able to add their own testimonial by filling out the form. Once they have created a review, they will be able to edit or delete their own review.
If they aren't logged in, a message will appear inviting them to login or register to write a review. 
A superuser is able to edit or delete any of the reviews on the page. 

##### Contact Page 
The contact page allows any user to fill out a form and send a message to the store owner. If the form is valid on submit, the user will view a success message. 
If the user is logged in, the form will be populated with their name and email.
This page also contains a simple google maps api map to allow the user to see where the store is actually located so they can visit.

##### Profile page
The main goal of the profile page is to allow the user to insert their billing/shipping information. If the user is logged in during checkout or when trying to fill out the contact form, 
their personal information will already be populated. On the profile page, the user will be able to view their past orders and click on them to once again view the order summary. The profile link in the navbar is only available to users who are logged in.

##### Login/Register
Created with Django- Allauth, the login and register has all of the standard features to create a new user. Styling was customized to make it unique.
There are pages included to handle:
* Sign up - requires username, email, password twice and an email will be sent with a verification link

* Login - requires either username or email and password with a toast message confirming successfully signed in

* Logout - Once completed logout, a toast message confirming successfully logged out

* Forgot password - requires email and email will be sent to link to update password

##### Cart
If no items are in the cart and the user navigates to the cart page, they will view a message that reads "There are no items in your cart". They will also be presented with a button that asks
if they would like to continue shopping that redirects to the shop page. If the user does have items in their cart, the items will be displayed in a table, with the options to update the quantity of the product or delete the product.
If the user amends a products quantity to zero, the item will be removed from the cart.
Once an item is added to the cart the total quantity is displayed on the Cart icon in the Navbar. 
A free delivery threshold exists, if the total price is below the free delivery threshold, a small message will appear letting the user know how much money is required for free shipping.
At the bottom of the page, if the user selects the checkout button, they will be taken to the checkout page. If they select the other button, they will be directed to the shop page to continue adding more products.

##### Checkout
If a user has added any items to their cart and clicks the Checkout button at the bottom of the page, they will be taken to the checkout page.
Here the user adds their details to an input form and can select whether to save the information to their profile for future purchases. 
The user will also be able to see an order summary of the items they plan to purchase as well as a grand total and cost of shipping (if applicable).
The user is also able to click a button to return to the cart if they would like to make any changes to the cart.
Once the order is submitted, an overlay with a spinning arrow is shown to let the user know their order is being processed.
After the order has successfully been completed, a checkout success page is shown. This page will only be shown when the user completes checkout or revisits the 
order history page and clicks on an order number in their profile.

##### Admin
Only available to the superuser/admin, this page allows the user to add new products to the database, including an image. If the form is valid, it will bw submitted to the database 
and can be viewed on the shop page. The admin is also able to navigate to any product in the store's one product page and be able to edit or delete the product.
The defensive design is implemented to restrict other than admin users to manually enter the url to get access to the page. If tried, the user will be redirected to the home page with a toast error message.


### Features Left To Implement

* 404 Errors required for instances where usher visits an unavailable page
* After successfully ordering a product, email confirmation is sent for order
* A page for the staff to see all orders made my customers, for fulfillment purposes to track orders completed and orders to do
* Star rating for reveiws and reviews for individual products
* To be able to signup/login through social media acounts facebook and google
* A reset password feature for logged in users, in case the user forgets their password
* Add a custom item where the user can add a specific size and color of their choosing to the cart
* A wishlist for users to save items they would like to purchase later



## Technologies

Languages, Frameworks, Editors & Version Control:
* HTML
* CSS
* JavaScript: to make Stripe elements, ShareThis button and dataTables work and to add the django-countries dropdown.
* Django: web framework version 3.0.8
* Python: Python3 is used as programming language
* Pillow: to be able to upload images
* Allauth: addressing authentication, registration and account management
* Stripe: to enable the user to make payments and check credit cards
* Crispy-forms: to easily make the forms and make them user-friendly.
* Bootstrap: to customise the html and make it responsive to different devices.
* JQuery:  For the Modal and Responsive Navbar expand & collapse functionality.
* Gitpod: used as IDE
* Heroku: used as deployment platform
* Google Maps API- to show a simple map 
* Pillow 4.3.0 - The Python Imaging Library adds image processing capabilities to your Python interpreter. This library provides extensive file format support, an efficient internal representation, and fairly powerful image processing capabilities. https://pillow.readthedocs.io/en/stable/handbook/overview.html
* Jinja - This is a modern and designer-friendly templating language for Python. It is fast, widely used and secure with the optional sandboxed template execution environment. https://jinja.palletsprojects.com/en/2.11.x/ 
* Stripe 2.46.0 - Checkout creates a secure, Stripe-hosted payment page that lets you collect payments quickly. It works across devices and is designed to increase conversion. Checkout makes it easy to build a first-class payments experience. https://stripe.com/docs/payments/checkout 
* Boto3- The Amazon Web Services (AWS) SDK for Python. It enables Python developers to create, configure, and manage AWS services, such as S3.
* AWS S3 Bucket- Used to store static and media files in production
* Gunicorn- A Python WSGI HTTP Server to enable deployment to Heroku
* Psycopg2- needed to enable the PostgreSQL database to function with Django

Template- Code Institute
The template provided by Code Institute is used as basis (https://github.com/Code-Institute-Org/gitpod-full-template.git). A repository was created on GitHub by choosing the green "Use this template" button.



## Testing

### Testing User Stories
All user stories have been verified and have passed their tests.
##### Shopper:
> 1 : As a shopper, I want to be able to view a list of products, so that I can choose one to purchase                                                        

The first of the shopper user stories highlights the importance of viewing all products in one area. This is achieved in the products/shop page where the user can view a list of all the products currently in the database.

> 2 : As a shopper, I want to be able to view product details, so that I can identify price, description, and image                                        

To go along with the minimalist theme for the site, it was decided to have the additional details of the product on a separate page from the one where the user can view all products together. Once a user clicks on the image or button
on one of the cards on the products page, the user will be taken to a specific page where they can view all details of the product and add a nummber of that item to their cart.

> 3 : As a shopper, I want to be able to view the cart at anytime, so that I can manage my purchase                                                         

This is accomplished by being able to click the cart in the navbar, located at the top of the screen. The sticky class was applied to the navbar so as to have this feature available at all times for the user. If the user has items in their
cart, they will also be able to view a grand total on the navbar.

> 4 : As a shopper, I want to be able to adjust the quantity of items in my cart or completely remove them, so that I can manage my purchase                                                         

In the cart page, if the shopper has items in their cart, they will be able to view a table of the contents in the cart. In this table, they will be able to adjust the quantity of the item or remove it completely by clicking the respective button
or changing the quantity to zero.


##### Site User:
> 5 : As a site user, I want to be able to register for an account, so that I can have a personal account to view my profile                                    

When the user clicks on the "My Account" button in the navbar, they will be able to view a dropdown with the options to register or login to the website.
Using Allauth authentication system and custom styling, the user is able to register, get an email confirmation, and then sign in to their account. 

> 6 : As a site user, I want to be able to login and logout, so that I can easily access my personal information                                         

After registering for an account and verifing their email, the user will be able to login via the login page. If the form is valid when submitted, the user will be logged in.
When the user is done browsing and would like to sign out, they can once again navigate to the navbar, click the "My Account" button, and select "Logout".

> 7 : As a site user, I want to be able to recover my password , so that I can recover access to my account                                                  

On the login page, the user has the option to recover their password by clicking the button "Forgot password". This will prompt the user to enter their email
and a link helping them to reset their password will arrive. A future feature to add to the site is to add a "Reset password" function to the profile page to allow the user
to reset their password when already logged in.

> 8 : As a site user, I want to be able to receive an email conformation, so that I can verify my registration was successful                                         

After filling out the registration form, the user will be sent an email with a link to confirm their email. Opening this link will prompt the user to click to comfirm 
that this is their account. Once the email is confirmed, the user can sign in.

> 9 : As a site user, I want to be able to have a personalized user profile, so that I can view my personal information such as payment information and order history 

Once authenticated, the user can view their profile by going to the same "My Account" button in the navbar and selecting "My Profile". Here they will view a greeting to their name and/or username,
a form to save their prefered shipping information, and a table that contains their order history (if applicable). 

> 10 : As a site user, I want to be able to contact the store owner with any questions

If the user clicks on the "Contact" button in the navbar, they will be taken to a contact page where the user is able to fill out a form that will be sent to the store owner. If the user is logged in and their name
and email are saved to their profile, these fields will automatically be populated. The user is also able to view the address and map of the physical stoe by means of Google maps.


##### Customer:
> 11 : As a customer, I want to be able to leave a review, so that I can leave my testimonial and support this small business                          

If the user clicks on the "Gallery" button in the navbar, they will be taken to a page to view photos of other people's orders as well as cards that contain reviews.
Any visitor to the site, logged in or not, is able to view these reviews. Users who are logged in have the ability to add a review by the review form located just below the review cards.
If the form is valid when submitted, the user's review will appear next to the other reviews.

> 12 : As a customer, I want to be able to edit my review, so that I can edit my previously created review with new details                            

If the user is logged in and has previously created a review, they will be able to see two buttons on their review card to either edit or delete their review. Clicking the edit review will take the user
to a new page where they can edit their review. If the form is valid when submitting, their review will update and they will be taken back to the gallery page. Previously I had designed this function to be in a modal, however due to many errors, it was decided upon to move this form to its own page (More details in the bugs section).
Clicking on the delete button on the review card will bring up a modal asking the user if they are sure they want to delete the review. Clicking confirm will carry out the action of deleting and the review will be removed from the database.

> 13 : As a customer, I want to be able to sort the list of products, so that I can view the available products by the size I prefer                              

If the user clicks on the "Shop" button in the navbar to visit the page with all products, they will be able to see a group of buttons where they can select the category they would like to browse. To the right of this group of buttons, 
there is also a dropdown that gives the user the ability to sort by price (most expensive - least expensive  or vise versa) or by mug size.

> 14 : As a customer, I want to be able to search for a product by name or description, so that I can quickly find the product I am interested in                                   

In the footer located at the bottom of all pages, the user can see a search bar. Entering any word or short phrase in the search bar, then clickung the button beside it will allow the user to search all products in the database. Results will come up if there is a match in the name or description. 
If no results or the user does not submit a valid search, an error message will show, inviting the user to try again.

> 15 : As a customer, I want to be able to view items in my bag to be purchased, so that I can identify the products and total cost before I purchase                        

Navigating to the cart, either from the navbar or in the toast message after adding an item to the cart, will allow the user to view a table of all items in their cart. A subtotal is calculated
at the right of the table (product price * quantity). A grand total is located at the bottom.
Once clicking the checkout button at the bottom of the page, the user will also be able to view a preview of the items they will purchase.

> 16 : As a customer, I want to be able to adjust the quantity or remove items in my bag, so that I can easily make changes before checkout                                           

When the user is on the cart page, they will see a table of all the products currently in the cart. There is a quantity selector to allow the user to change the quantity of the product in their cart. Clicking "update" 
will save the changes. Clicking the delete button or setting the quantity to zero will remove the item from the cart.

> 17 : As a customer, I want to be able to enter my payment information, so that I can check out easily with no problems                                             

From the cart page, there is a button at the bottom of the page inviting the user to "checkout". This will bring them to the secure checkout page where they can enter their shipping information and payment information.
If the user is logged in and has their shipping information saved in their profile, these fields will already be populated.

> 18 : As a customer, I want to be able to view an order confirmation after checkout, so that I can verify there are no mistakes with my address, order, or payment information   

If the checkout form on the checkout page is valid when submitted, an overlay with a spinning arrow will appear letting the user know their order is being processed. Once the payment process has completed, the user will 
see a success message, their previously entered shipping details, as well as a summary of what they ordered. If the user is logged in, they can once again view this page from the "My account/"My Profile" page.


##### Store Owner:
> 19 : As a store owner, I want to be able to add a product, so that I can add a new item to my store                                                    

If the user is a superuser and is logged in, they will be able to view an additional page in the "My Account" dropdown on the navbar called "Management". Clicking on this page will bring up a form to allow the superuser
to add a new product to the store. When the form is valid on submit, the new product will be added to the shop page and the superuser will be directed there. If the user is not a validated superuser, they will not be able to access this page.

> 20 : As a store owner, I want to be able to edit a Product, so that I can change any details in the price or description                                

Navigating to a single product's page from the shop page will allow the user to view two additional buttons that other users will not be able to see, "edit" and "delete". Clicking on the "Edit" button will allow the superuser to access an editing form
for the product they are currently looking at. If the form is valid on submit, the product will be updated, and the user will be taken back to the shop page.

> 21 : As a store owner, I want to be able to delete a Product, so that I can remove items that are no longer available                                     

Navigating to a single product's page from the shop page will allow the user to view two additional buttons that other users will not be able to see, "edit" and "delete".  Clicking on the delete button will remove the product from the store.

> 22 : As a store owner, I want to be able to edit and delete reviews, so that I can manage customer reviews                                        

If the superuser clicks on the "Gallery" button in the navbar and navigates to the reviews, they will be able to see two additional buttons on every review, "edit" and "delete". The superuser has the ability to edit or delete any review. Clicking the edit review will take the user
to a new page where they can edit their review. If the form is valid when submitting, their review will update and they will be taken back to the gallery page. Previously I had designed this function to be in a modal, however due to many errors, it was decided upon to move this form to its own page (More details in the bugs section).
Clicking on the delete button on the review card will bring up a modal asking the user if they are sure they want to delete the review. Clicking confirm will carry out the action of deleting and the review will be removed from the database.

> 23 : As a store owner, I want to know if a contact form has been submitted, so I can write a reply to my customer

If a customer has submitted a contact form, the superuser email that is set up with the account will recieve a message (see the picture below). A future feature that I would like to add to the site is for the user to be able to view the contents of the message in a page on their profile and be able to respond directly from this website.




### Manual Testing

##### Navigation Bar

##### Footer

##### Home

#### Shop

##### One Product

##### Gallery

##### Contact

##### Profile

##### Management

##### Login/register

##### Cart

##### Checkout



### Validation
Validator websites were used to test the following:

HTML - W3C Html Checker:
Doing so brought up a few errors throughout the project related to using Django templates. These included an issue in using '{}' brackets as part of the source for <a> elements and <img> elements. However, this syntax is necessary to access static files and urls and was therefore ignored.
All html templates led to errors that the doctype and language were not declared. As the templates were based on the base.html template where these were addressed, this issue was also ignored.
Some Bootstrap Modals on the site returned errors with their 'aria-labelledby' attribute. This error was related to using templating language to specify the item the modal was related to, so this error was also ultimately ignored.

CSS - W3C CSS Checker - No errors found

JavaScript - JSHint - No errors found

Python - PEP8 Online Check - a number of whitespace and lines too long warnings.
The command "python3 -m flake8" was also run in the terminal to fix problems with code. The only problems found were due to whitespace or lines that were too long.


### Browser testing
This website was tested on multiple devices with varying screen sizes and in multiple browsers. All devices and web browsers passed testing.

Web Browsers:
* Google Chrome
* Safari
* Firefox

Devices:
* Macbook
* iPad Pro
* iPad Air
* iPhone x
* iPhone 11
The primary method of testing the browsers was to ask several users to visit the website using these different devices and web browsers. Each user was asked to complete a test purchase, register and login to a new account, and create, edit, and delete their reviews.

### Found Bugs and fixes


## Deployment
This project was developed using the Gitpod environment. It used Gitpod for version control. The project was regularly committed to GitHub after each crucial piece of coding.
The deployed project can be viewed on the following link: 
The project's GitHub repository can be viewed with the following link: 

### Local Deployment
If you would like to further contribute to this project, you can clone it to your local machine using the following steps:

1. Select the Repository from the Github Dashboard.

2. Click on the "Clone or download" green button located above and to the right of the File Structure table.

3. Click on the "clipboard icon" to the right of the Git URL to copy the web URL of the Clone.

4. Open your preferred Integrated Development Environment (IDE) and navigate to the terminal window.

5. Change the current working directory to the location where you want the cloned directory.

6. Enter the following command and press 'Enter' to create your local clone:
        
        git clone https://github.com/amybru/mug_shots

7. Install the required dependencies. Add the following command to the terminal:
        
        pip3 install -r requirements.txt

8. Add the environment variables. If using Gitpod, the environment can be set in the settings. Or you can create an .env file. Add your env.py file to .gitignore to make sure your database information is not viewable to others and to keep your values safe. Add the following values:
        
        SECRET_KEY
        STRIPE_PUBLIC_KEY
        STRIPE_SECRET_KEY
        STRIPE_WH_SECRET
        DATABASE_URL
        DEVELOPMENT = True

9. To set up the Django SQLite3 tables required for this project, use the following commands:
        
        python3 manage.py makemigrations
        python3 manage.py migrate

10. Create a Superuser for your project to work as an admin. Add the following command to the terminal, then create username and password for the superuser.
        
        python3 manage.py createsuperuser

11. You can now run the cloned application to test it using the following command:
        
        python3 manage.py runserver


### Heroku
To deploy the project to Heroku, follow the steps above in "Local Deployment", then complere the following steps:

1. Register/sign in for Heroku.

2. Once signed in, click the "new" button on the dashboard to create a new application.

3. Name the App and choose the region you are currently in.

4. To use the Postgres database for deployment, select 'Heroku Postgres' as a free add-on.

5. After the app is created, go to the 'Settings' tab and click on the 'Reveal Config Variables' button. Input the following values:

| Key               | Value                                   |
|-------------------|-----------------------------------------|
| DATABASE_URL      | Heroku Postgres database url            |
| SECRET_KEY        | secret key used for your Django project |
| STRIPE_PUBLIC_KEY | obtained through your Stripe account    |
| STRIPE_SECRET_KEY | obtained through your Stripe account    |
| STRIPE_WH_SECRET  | obtained through your Stripe account    |
| ADMINS_EMAIL      | email admin for the emails feature      |
| GOOGLE_MAP_KEY    | obtained from google maps api           |  

6. Create a requirements.txt file in your gitpod terminal/
        
        pip3 freeze --local > requirements.txt

7. Create a Procfile with the following content
        
        echo web: gunicorn mug_shots.wsgi:application > Procfile

8. Set up the database with Postgres.
        
        python3 manage.py makemigrations
        python3 manage.py migrate

9. Create a Superuser for your project to work as an admin. Add the following command to the terminal, then create username and password for the superuser.
        
        python3 manage.py createsuperuser

10. You can now run the cloned application to test it using the following command:
        
        python3 manage.py runserver

11. Commit these changes to your repository:
        
        git add .
        git commit -m "<your commit message here>"

12. With these changes made and commited in gitpod, log into heroku and enter your login credentials.
        
        heroku login -i

13. Once you have successfully logged into Heroku from the terminal, link your Heroku app to your remote repository
        
        heroku git:remote -a <your app name here>

14. Finally, push the project to Heroku

        git push heroku master

##### Hosting media files with AWS
The static files and media files for this project are currently hosted in an AWS S3 Bucket. To host them, you need to create an AWS account and create your S3 bucket, making sure to allow public access.
After creating an account and uploading the files, the following environment variables should be added via the settings or .env file.
        USE_AWS (set to True)
        AWS_ACCESS_KEY_ID
        AWS_SECRET_ACCESS_KEY

##### Sending Emails with Gmail
In order to send real emails from the website, you must connect it to a Gmail account. 
Either use an existing Gmail account or create a new one, then sign in and navigate to the Google Account Security page. From here, create two-step authentication by creating an App password for a Django app. 
Add the following environment variables to your settings or .env file.
        EMAIL_HOST_USER
        EMAIL_HOST_PASS


## Acknowledgement
I would like to thank and credit the following sources for their assistance and contribution to this project.

* My mentor with Code Institute, Gerard McBride, for helping me to brainstorm and coaching me through this project

* The tutoring Team at Code Institute for helping me fix several bugs and understand why these errors were happening

* A big thanks to my friends and peers for helping me test the site extensively, to make sure each feature worked as expected on various devices.



## Credits

##### Images
All Images are taken from Unsplash.

##### Icons
Icons are from Font Awesome.

##### Fonts
All fonts are from Google Fonts.

##### Wireframes
The wireframes attached to this README were created using Balsamic.

Prices, names, and descriptions on all products are fictional.

##### Code
Much of the code is inspired by the Boutique Ado mini project from Code Institute. Their tutorial videos assisted me in creating
many of the apps required for this project, including: the checkout app and the add to cart functionality.

> NOTE: This project was created for educational purposes only as 'Mug Shots' is a fictional business.