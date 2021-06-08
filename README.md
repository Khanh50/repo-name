# BLUETH : A web application that helps you learn new words via flashcards
#### Video Demo:  <URL HERE>
#### Description:
Blueth is a web application that help everyone learn vocabulary by using the same idea as flashcard. It provides a website where users can create and practice with virtual flashcards. When users practice with their flashcards, the order of flashcard depends on users' fluency, flashcards with words which users more fluent will appear last.
This project contains following files: application.py, style.css, add.html, index.html, layout.html, login.html, register.html, setting.html, language.csv, project.db.
1. application.py:
    - This is the backend of Blueth, written in Python. It is responsible to input new datum form users to database, send specific datum to users, process information received from users and send reponses.
    - application.py contains these following main functions responsible for most of web's work: index, login, logout, register, add, setting.
        - index is the first function to be called when users visit Blueth, it will redirect users to route /login if users have not logged in. When users have logged in, index will take from datebase users' flashcard(s) and send them to index.html. Beside that, index also keep track of users' fluency when they practice, but users have to reload the page for newly updated fluency in next time they practice.
        - login take usernames and passwords privided by users then take a look at database to make sure if those information is valid. If valid, login will redirect users to homepage.
        - logout redirect users to /login, and log out users' account.
        - register input new users information to database.
        - add is function that add new flashcards to users' list of flashcards. Flashcards' details is inputted by users via a form.
        - setting will either delete users' card, users' account, change username or password when it receives sygnal from setting.html.
2. style.css: The aesthetic of the page is decided by this file.
3. index.html: The Blueth homepage, where users can see their flashcards and practice with them.
4. login.html: This file displays the Login Page, users send their username(s) and passwords via this page.
5. register.html: Where users register for new account if they have not had one.
6. setting.html: Users can delete their set of cards, their account, or change their username (or password) here.
7. layout.html: Help display the repeated contains throughout other page.
8. language.csv: Contain languages' name and their ISO language code. This file is used in add.html for the sake of searching via Google Translate.
9. project.db: Have two tables, users and cards.
    - users: Contain users' information such as their username, password, id,...
    - cards: Contain cards' information, which is entered by users themself, such as what the word is, type of the word, it's meaning,...
