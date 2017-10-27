# Hair Salon
### A Hair Salon Management Application for Epicodus C# Database Basics Code Review _10.20.2017_

#### By Kimberly Bordon

## Description
_This is an application that exercises the basics of accessing databases and one-to-many relationships using C# and MySql. The application allows the user to manage the stylists, and the stylists' clients of a specific hair salon._

# Specs
|Behavior|Input|Output|
|-|-|-|
|The app will start user at the hair salon homepage to either add or view the current stylists.| The user goes to homepage.| The user is presented with homepage with title, and two links to either add or view current stylists.|
| Will allow user to see all the hair salon's current stylist. | The user clicks "View Stylists" link on the homepage. | The user is taken to new page that lists all stylists |
| Will allow user to go to form to enter a new stylist's information. | The user clicks "Add a Stylist" link on homepage. | The user is taken to a new page with a form to enter the new stylist. |
| Will allow user to fill form and add a stylist to list of stylist. | User enters: <br><br>Dylan Brook<br>503-444-6745<br><br> User clicks Submit | The user is taken to list of stylists, with newly added stylist. |
| Will allow user to select a stylist from the list, and see their information and clients. | User clicks a stylist name. | The user is taken to stylist's detail page, including list of client if they have any. |
| Will allow user to select a client from the stylist's list of current clients, and see their information. | User clicks a client's name. | The user is shown client's information. |
| Will allow user to add new clients to a stylist's client list. | User clicks "Add a Client" on stylist's detail page. | The user is taken to page with a client form. |
| Will allow user to fill out client information, and add client. | User enters:<br><br>Dahlia Miyazaki<br>503-859-3324<br><br> User clicks Submit | The user is taken to stylist's page of that client with client newly added to client list. |
| Will allow user to update a client's information details. | User clicks on edit link on the client's information, and enters new information.<br><br>User clicks Submit. | The client's information is updated, and the user is taken back to stylist page with new client information shown.|
| Will allow user to delete a client that no longer visits the salon. | User clicks on client's name on stylist's page. User clicks on "Delete" button on client's information page. | User is taken back to stylist page with list of clients without just removed client. |

## Setup/Installation Requirements
* Enter the URL: https://github.com/kbordon/csharp-week3-code-review-hair-salon in your browser.
* Using your terminal or powershell, clone this repository by typing ```>git clone https://github.com/kbordon/csharp-week2-code-review.git```
    * Alternatively, you can use a browser to download the .zip file from the Github web interface at the URL: https://github.com/kbordon/csharp-week2-code-review
* Navigate to the project folder csharp-week2-code-review, and use a text editor like Atom to open the README.md.

```SQL
>CREATE DATABASE kimberly_bordon;
>USE kimberly_bordon;
>CREATE TABLE stylists (id serial PRIMARY KEY, name VARCHAR(255), phone VARCHAR(255));
>CREATE TABLE clients (id serial PRIMARY KEY, name VARCHAR(255), phone VARCHAR(255), INT stylist_id);
```
## Known Bugs
* When listing phone numbers, should a zip code be entered starting with a zero, the number may be listed without the zero as it is converted into a number, and will lose the beginning number.
