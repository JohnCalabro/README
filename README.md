Side Note - I wanted to turn in this README.md alone to showcase here. I will add this README.md to the main project and upload everything to GitHub, when finalizing it. 

This is my very first application. I plan to add more to it down the line. To get this app up and running you must fork this project and set up a virtual environment in a fresh directory , then you must refer to the requirements.txt file so you can download all dependencies (it is suggested you create and activate the new venv and download all dependencies BEFORE doing anything else,  bcrypt gave me issues when I tried to import it at first,  what helped fix this was updating pip but I am still not 100% sure what the reason behind the import error was) Next you must run a server form the directory within your virtual environment. You also need access to my database on PostgreSQL.

This app serves as a Pokemon Team Builder. In this application you can type a Pokemon’s name into a form to locate the pocket monster, and can afterwards add that Pokemon to your team. Once all added you are able to view all of your teams displayed in rows of six, each row stacked upon the other. You are limited to building only 6 teams. You can also click links to view each team individually and view their details. So far I only display the name and sprite of the Pokemon, but I plan to add more details such as type and perhaps some suggested move sets in the future.

This application requires users to sign up for a User account,  to sign up all you need to do is create a username and password. The passwords are secure because I used bcrypt to obfuscate the passwords, now I will discuss the technologies that are used in the app. 

Technologies: 

This is a Flask application which is built on Flask. This app is written in mostly Python and JavaScript. This application also uses jQuery in some JS files, as well as axios for API requests, these requests are sent to the pokeapi -  https://pokeapi.co/ 

As mentioned above I use bcrypt to protect the passwords of users making the app more secure. In terms of styling I have used Bootstrap’s grid system, other than that styling is minimal, I plan to add more styles in the future. You can view every external resource in my requirements.txt file. I also used psql to create my own database that I populated with ids from the pokeAPI.

(note - still need to add requirements.txt file, will do so when I upload this with the project eventually)

Needs for Improvement:

So far the app merely displays the Pokemon’s sprite (images from hand-held games) and Pokemon names. I will  eventually display more details about the Pokemon including their types among other stats. This app allows you to delete an account and delete teams, however so far it does not allow you to edit teams, this is mostly a strategic choice because I do not feel it necessary for a user to be able to edit the team at this point since there are merely 6 teams allowed, it is easier if a user deletes one and starts from scratch.

 If anyone who might use this app would prefer an edit feature I would consider adding that. A second reason why I omitted an edit team feature is that the data stored in my psql database is all integers, and due to time sensitivity I decided that associating these integers with the actual Pokemon  names in my app.py route was very involved logic wise, but I will keep this feature in mind. 