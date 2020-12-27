# Hit the Slopes! - TESTING
## Let's Team Up & Hit the Slopes! - TESTING
#### Data Centri development Project - Testing write-up

<img src="static/readme/amiresponsive_main.jpg" alt="Title image" style="margin: 0 10px;" width="100%"/>

This document is intended to record testing at various stages of development of the project, as well as different functions, functionalities, correct display of the project's page, etc. 

[Main README.md file](README.md)

[View website on Heroku](https://hit-the-slopes.herokuapp.com/)

## Hit the Slopes app

## Table of Contents
1. [**Automated Testing**](#automated-testing)
    - [**Validation services**](#validation-services)
2. [**Client Stories Testing**](#client-stories-testing)
3. [**Manual Testing**](#manual-testing)
    - [**Testing undertaken on laptop**](#testing-undertaken-on-laptop) 
    - [**Testing undertaken on mobile and pad devices**](#testing-undertaken-on-mobile-and-pad-devices)
    - [**Testing undertaken in DevTools**](#testing-undertaken-in-DevTools)
4. [**Bugs discovered**](#bugs-discovered)
    - [**Solved bugs**](#solved-bugs)
    - [**Unsolved bugs**](#unsolved-bugs)
5. [**Further Testing**](#further-testing)


## Automated Testing

### Validation services
The following validation services were used to check the validity of the website code.
- [W3C Markup Validation]( https://validator.w3.org/): 
    * Using individual page links for validation: No errors or warnings.
    * Using source code of each page: errors due to repeated ID of users, because one username, in multiple trips created by the user. Plus  repeated ID in See profile link to open a user's profile. 
- [W3C CSS validation](https://jigsaw.w3.org/css-validator/):
    * Validating the file with the last commit: e1b34f2, link - https://github.com/OlekSt/Hit-the-Slopes/commit/e1b34f25a5d35447c0c1383a293113c1e445d685.
    * No errors on validating the source code from here https://raw.githubusercontent.com/OlekSt/Hit-the-Slopes/master/static/css/style.css
    * Three errors from materialize.min.css, and numerous warnings to materialize.min.css, if validating the deployed website on heroku. 
    **These errors were indicated in my initial submit!!!**
    **I still don't understand why the assesment came back with CSS errors**
    * See printscreens
- [JSHint](https://jshint.com/):[1](static/re_submission/css_validation01.jpg), [2](static/re_submission/css_validation02.jpg), [3](static/re_submission/css_validation03.jpg) 
    * No errors, 3 warning about 'let' & 'const'.
- [PEP8 Python Validator](http://pep8online.com):
    * Checking the file commited on 27.12.2020, link to raw file https://raw.githubusercontent.com/OlekSt/Hit-the-Slopes/master/app.py
    * No errors or warnings.
    * See printscreens: [1](static/re_submission/python_validation01.jpg), [2](static/re_submission/python_validation02.jpg), [3](static/re_submission/python_validation03.jpg) 
- [Am I responsive](http://ami.responsivedesign.is/) was used to check responsiveness of the website for various screen sizes - mobile, tab, laptop, desktop. 

##### back to [top](#table-of-contents)


## Client stories testing
The user stories are described in the UX section of [README.md](README.md) 

**As a website visitor, I want:**

1. I want to find other people with similar interests to meet them during my skiing holidays
    * I can clearly see what the website is about from the index page, where I see the slogan "Start or Join a snow Team"
    * I can clearly see from the start (on index page) what steps I need to take:
        - Sign Up
        - Post your trips
        - Search other users' trips
        - Team Up with other people
        - Go skiing/snowboarding
    * On Sign Up I can add my name or nickname, and provide info about my age, and where I am from, plus choose a cool avatar for myself
    * I can easily see a list of ski resorts and search for ones I am interested in
    * I can see a list of upcoming trips starting from current/today's date

2. I want to easily add details of my trip to the DB
    * When I check ski resorts I can see what ski resorts I choose from, with a brief title to give me a general idea about it, in case I am not familiar with it. 
    * From a ski resort's account I can go directly to its official web-site, and to check its location on Google maps
    * I can create my own trip with necessary info:
        - Dates of my trip
        - To which ski resort I will go
        - Who i will go with, adults, kids, alone, etc. 
        - What I prefer - skiing or snowboarding
        - Provide additional info about me, my friends, or my kids (age, for example), or my interests

3. I want to be able to check for already added trips and see if I’m interested to connect to other people
    * Trips show me:
        - A user who created a trip, including a user's profile, where I can see info about this user, and have an option to contact this user
        - Dates of this planned trip
        - To which ski resort
        - How many adults and go
        - What they prefer - skiing or snowboarding
        - Some additional info posted by a user
    * Based on the provided info described before I can decide which trips/users I am interested in    

##### back to [top](#table-of-contents)

4. I would like to contact other users
    * I can check users' profiles from trips they created
    * I can contact users and plan discuss possible meeting at the ski resort

5. I want to add locations if not yet in DB
    * If a ski resort is missing I can create one
                Note: If a user creates a ski resort, and later a manager wants to create a ski resort, the website owner will contact this user, and hand over rights to manager this ski resort's account to its official representative.

6. I want to see all trips for the next two months to a chosen location, and see if I’d plan my trip together with some other people
    * I can easily search trips by a ski resort's name, start and end dates, or any combination of those.
    * I can check for past trips, and contact users' and potentially plan some future trips if they go to locations I like


**As a ski resort manager, I want:**:

1. I want to add my ski resort to the DB so users don’t have to do that
    * I can clearly see what the purpose of the website is
    * I can sign up and create an account for my ski resort for users to plan their trips and them to the list of upcoming trips
    * Only I can modify into on the account or delete the account permanently

2. I want to provide most important info about my ski resort
    * I can add correct name of my ski resort
    * I can add website and Google map links to the account

3. I want to provide correct links to my website
    * I can provide the correct link to my ski resort website
    * I can provide a correct Google map link to a place within the ski resort I consider the best location

4. I want to advertise my location and promote upcoming events
    * I can discuss possible advertising options on the web-site with the web-site's owner


##### back to [top](#table-of-contents)


## Manual testing
The section described in detail all the steps taken to confirm all the elements of the website work as intended. 
Tested on:
- laptop
- pad mode on a laptop
- mobile phone
- Chrome Developer Tools device simulators on all options
*Friends tested on various devices - desktops, pads, mobile phones; Android and Apple.*

### Testing undertaken on laptop
The website was tested on Lenovo Yoga 530, in Google Chrome, Mozilla Firefox, Microsoft Edge, Brave browser

1. The main page screen:
    - Confirmed that it shows the main screen with the slogan "Join/Start a snow team" with a list of actions required: Sign up, Post Trips, Search Trips, Team Up, Hit the slopes (each with a descriptive icon).
    - Confirmed that SignUp action points to sign_up.html, and Post Trips, Search Trips, Team Up actions point to sign_in.html. Used button back to go back to the main screen with no issues.
    - Confirmed that the navbar has the Logo and links to Sign Up and Sing In, pressing on the Logo takes us back to the main screen(index.html), and both Sign Up & Sing In take to respective pages.

2. Sign Up screen:
    - Confirmed that pressing the Logo takes me back to the main screen(index.html), and pressing Sing In takes me to sign_in.html.
    - Confirmed that the registration process works, and validation does not allow to register with any field left empty. If not, a message is flashed next to a field, which still needs info. Gender, age fields open correct select dropdown menus. Avatar dropdown menu opens a correct list of avatars with images and names.
    - Confirmed that pressing Sign Up buttons takes me to the trips.hmtl, flashes a message "Welcome, 'username'!", shows the list of trips, and the navbar shows full (visible to logged in users) menu with the Logo, Trips, New Trip, Ski Resorts, New Ski Resort, Copyright, Sign Out. Plus search window with fields: Ski Resort, Date from, Date to, and buttons: Reset & Search.

##### back to [top](#table-of-contents)

3. Sign In screen:
    - Show correct screen with a name and a password fields. The navbar has the logo, which takes us to the main screen(index.html) and Sign Up, which takes to sign_up_page.html, and Sign In, which takes to the sign_in_page.html.
    - Confirmed that sign in process requires both name and password fields to be filled in. If not, a message is flashed next to a field, which still needs info. 
    - Tried to sign in with a wrong password, flashes the message "Wrong password. Try again".
    - Tried to sign in with a wrong name, flashes the message "Wrong name. Try again".
    - With correct name & password correctly takes us to the trips.html, flashes a message "Welcome back, 'username'!", shows the list of trips, and the navbar shows full (visible to logged in users) menu with the Logo, Trips, New Trip, Ski Resorts, New Ski Resort, Copyright, Sign Out. Plus search window with a fields Ski Resort and buttons: Reset & Search.

4. Trips screen:
    *Navbar*
    - Pressing on the logo takes us back to the trips (when users are logged in), the flashed welcome message disappears.
    - Pressing Trip on the menu takes us back to display trips.
    - Pressing New Trip takes to the add_trip.html displayed correctly. 
    - Ski Resorts takes us to skiresorts.html
    - New Ski Resort to add_skiresort.html
    - Copyright opens a modal with a mini hero image, and info who designed and developed, and a link to the developer's Github.
    - Sign Out correctly signs out to index.html with the main screen with the slogan "Join/Start a snow team", where the navbar has the Logo, links to Sign Up & Sign In.
    *End Navbar*

    - Trips are correctly displayed with dates from today into the future in correct chronological order. 
    - Testing search with a ski resort name, it returns a list of trips to that ski resort in correct chronological order.
    - Dates search fields work correctly, once the Date-From is chosen, the datepicker for Date-To shows the chosen Date-From, and does not allow choosing dates before. and vice-versa, when Date-To is chosen first, the datepicker for Date-From will show that date, and won't allow choosing dates after.
    - Search for trips before today, shows a list of trips correctly, which are not visible on the general trips display, which shows them from today into the future. 
    - Rest button works correctly and returns a list of trips from today into the future in correct chronological order.
    - Searching by Date-From returns a list of trips starting that date in correct chronological order.
    - Searching by Date-To returns a list of trips before that date in correct chronological order, including trips before today.
    - Searching a combination of a ski resort and any of both dates, return a correct list of trips to that destination, starting a date or before a date. 
    - In all cases a correct message is flashed saying "Trips to 'ski resort'"; "Trips to a 'ski resort' between date-from & date-to"; or other correct combinations.
    - Pressing on Search button without any search info flashes a message "No search parameters were chosen" and shows a list of trips.
    - A trip in the list, shows a user's name and avatar image, who created that trip; ski resort's name with an thumbnail image, dates from and to, number of adults and kids going, ski vs snoboard preference, and additional note from that user.
    - Mouse over a user's name opens an action bubble, suggesting seeing a user's profile. Pressing on it shows a user's profile in a modal, with a name, avatar image, age range, place where user is from, and Contact link (confirmed that pressing it takes a user to contact_me.html).
    - Mouse over a ski resort's name opens an action bubble, suggesting seeing ski resorts, and confirmed that pressing it, takes us to skiresorts.html. 
    - Buttons to Edit or Delete a trip are visible only to a user who created that particular trip. 
    - A user/owner of a trip can press Edit, and will be taken to edit_trip.html, where all the previously saved data will be shown with a possibility to modify.
    - A user/owner of a trip can press Delete, and a trip will be deleted, user will be returned to the trips.html. A message will flash "'Username', we've deleted your trip." *Note: Feature to be added to ask a user for confirmation if he/she really wants to delete a trip.*

##### back to [top](#table-of-contents)

5. New Trip screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Confirmed that it won't allow to save a trip with any field empty, shows a message next to such empty field.
    - Confirmed that Choose a ski resort dropdown menu correctly opens a list of ski resorts which are already registered in the database.
    - Dates fields open datepicker, Date-From field does not allow to choose dates before today's. Dates search fields work correctly, once the Date-From is chosen, the datepicker for Date-To shows the chosen Date-From, and does not allow choosing dates before. and vice-versa, when Date-To is chosen first, the datepicker for Date-From will show that date, and won't allow choosing dates after, but also won't let choose dates before today's.
    - Confirmed that Date-To cannot be before Date-from and vice-versa.
    - Adults/Kids fields accepts only numbers from 0, don't allow negative numbers or letters. Shows a message that a correct value should be entered. 
    - Ski/Snowboard shows correct dropdown menu with Ski and Snowboard to choose from. 
    - Pressing Save Trip adds trip to the list of trips, and redirects a user to trips.html, where the list of trips is displayed. Buttons to Edit or Delete a trip are visible only to a user who created that particular trip. 

6. Edit trip screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - All the fields are populated with data previously saved in DB. If i press save without changing anything, all the data is kept as before. Same with pressing Cancel. 
    - If I change any data, and press Save, new data will be saved into DB. 
    - Upon saving a message is flashed "'Username', we've updated your trip."

7. Ski resorts screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Ski resorts are displayed in alphabetical order. 
    - A ski resort card displays its name, a short descriptive title, a thumbnail image, info whether it is a glacier, and if night skiing is possible, link to a ski resort's official website, and Google map link, with additional info field for any useful information about it.
    - Confirmed that both website and map links work and open a target website in another tab. 
    - Search card contains search field, plus Reset & Search buttons. 
    - Putting a name of a ski resort and pressing Search will return a card with a respective ski resort. 
    - If name is not in DB, it will return an empty screen, no ski resorts. 
            *To add a flashed message "Ski Resort is not found*
            *To add a feature to search by an initial/two/three letter/s*
    - Pressing Search with an empty search field, will show a message that the field has to be entered. 
    - Pressing Reset will display all the ski resorts in alphabetical order. 


##### back to [top](#table-of-contents)


8. New Ski Resort screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Confirmed that it won't allow to save with any field empty, except additional info field.
    - Website and map links are validated for an url to be entered. 
    - Glacier and Night skiing dropdown menus show correct choices.
    - Additional info field is not obligatory. 
    - Thumbnail dropdown menu shows correct list of images with names.
    - Pressing Add Ski Resort, saves the info into DB correctly (checked Atlas mongod DB), and takes us to the list of ski resorts in skiresorts.html.
    - Checked add_trip.html, a ski resort is added to the list.
    - Buttons to Edit or Delete a ski resort are visible only to a user who created that particular ski resort. 
    - A user/owner of a ski resort can press Edit, and will be taken to edit_skiresort.html, where all the previously saved data will be shown with a possibility to modify.
    - A user/owner of a ski resort can press Delete, and a ski resort  will be deleted, user will be returned to the ski_resorts.html. A message will flash "'Username', we've deleted your ski resort." *Note: Feature to be added to ask a user for confirmation if he/she really wants to delete a ski resort.*

9. Edit ski resort screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - All the fields are populated with data previously saved in DB. If i press save without changing anything, all the data is kept as before. Same with pressing Cancel. 
    - If I change any data, and press Save, new data will be saved into DB. 
    - Upon saving a message is flashed "'Username', we've updated your ski resort."

10. Sign Out
    - Pressing take us correctly to the index.html with the main screen with the slogan. The navbar shows only the log and Sign Up & Sing In links. 


##### back to [top](#table-of-contents)

### Testing undertaken on mobile and pad devices
The website was tested on Samsung A7 & Lenovo Yoga 530 in Pad mode, Google Chrome, Microsoft Edge & Mozilla Firefox
1. The main page screen:
    - Confirmed that it shows the main screen with the slogan "Join/Start a snow team" with a list of actions required: Sign up, Post Trips, Search Trips, Team Up, Hit the slopes (each with a descriptive icon).
    - Confirmed that SignUp action points to sign_up.html, and Post Trips, Search Trips, Team Up actions point to sign_in.html. Used button back to go back to the main screen with no issues.
    - Confirmed that the navbar has the Logo and links to Sign Up and Sing In, pressing on the Logo takes us back to the main screen(index.html), and both Sign Up & Sing In take to respective pages.

2. Sign Up screen:
    - Confirmed that pressing the Logo takes me back to the main screen(index.html), and pressing Sing In takes me to sign_in.html.
    - Confirmed that the registration process works, and validation does not allow registering with any field left empty. If not, a message is flashed next to a field, which still needs info. Gender, age fields open correct select dropdown menus. Avatar dropdown menu opens a correct list of avatars with images and names.
    - Confirmed that pressing Sign Up buttons takes me to the trips.hmtl, flashes a message "Welcome, 'username'!", shows the list of trips, and the navbar shows full (visible to logged in users) menu with the Logo, Trips, New Trip, Ski Resorts, New Ski Resort, Copyright, Sign Out. Plus search window with fields: Ski Resort, Date from, Date to, and buttons: Reset & Search.

3. Sign In screen:
    - Show correct screen with a name and a password fields. The navbar has the logo, which takes us to the main screen(index.html) and Sign Up, which takes to sign_up_page.html, and Sign In, which takes to the sign_in_page.html.
    - Confirmed that sign in process requires both name and password fields to be filled in. If not, a message is flashed next to a field, which still needs info. 
    - Tried to sign in with a wrong password, flashes the message "Wrong password. Try again".
    - Tried to sign in with a wrong name, flashes the message "Wrong name. Try again".
    - With correct name & password correctly takes us to the trips.html, flashes a message "Welcome back, 'username'!", shows the list of trips, and the navbar shows full (visible to logged in users) menu with the Logo, Trips, New Trip, Ski Resorts, New Ski Resort, Copyright, Sign Out. Plus search window with a fields Ski Resort and buttons: Reset & Search.

##### back to [top](#table-of-contents)

4. Trips screen:
    *Navbar*
    - Pressing on the logo takes us back to the trips (when users are logged in), the flashed welcome message disappears.
    - Pressing Trip on the menu takes us back to display trips.
    - Pressing New Trip takes to the add_trip.html displayed correctly. 
    - Ski Resorts takes us to skiresorts.html
    - New Ski Resort to add_skiresort.html
    - Copyright opens a modal with a mini hero image, and info who designed and developed, and a link to the developer's Github.
    - Sign Out correctly signs out to index.html with the main screen with the slogan "Join/Start a snow team", where the navbar has the Logo, links to Sign Up & Sign In.
    *End Navbar*

    - Trips are correctly displayed with dates from today into the future in correct chronological order. 
    - Testing search with a ski resort name, it returns a list of trips to that ski resort in correct chronological order.
    - Dates search fields work correctly, once the Date-From is chosen, the datepicker for Date-To shows the chosen Date-From, and does not allow choosing dates before. and vice-versa, when Date-To is chosen first, the datepicker for Date-From will show that date, and won't allow choosing dates after.
    - Search for trips before today, shows a list of trips correctly, which are not visible on the general trips display, which shows them from today into the future. 
    - Rest button works correctly and returns a list of trips from today into the future in correct chronological order.
    - Searching by Date-From returns a list of trips starting that date in correct chronological order.
    - Searching by Date-To returns a list of trips before that date in correct chronological order, including trips before today.
    - Searching a combination of a ski resort and any of both dates, return a correct list of trips to that destination, starting a date or before a date. 
    - In all cases a correct message is flashed saying "Trips to 'ski resort'"; "Trips to a 'ski resort' between date-from & date-to"; or other correct combinations.
    - Pressing on Search button without any search info flashes a message "No search parameters were chosen" and shows a list of trips.
    - A trip in the list, shows a user's name and avatar image, who created that trip; ski resort's name with an thumbnail image, dates from and to, number of adults and kids going, ski vs snoboard preference, and additional note from that user.
    - Touching a user's name opens an action bubble, suggesting seeing a user's profile. Pressing on it shows a user's profile in a modal, with a name, avatar image, age range, place where user is from, and Contact link (confirmed that pressing it takes a user to contact_me.html).
    - Touching a ski resort's name opens an action bubble, suggesting seeing ski resorts, and confirmed that pressing it, takes us to skiresorts.html. 
    - Buttons to Edit or Delete a trip are visible only to a user who created that particular trip. 
    - A user/owner of a trip can press Edit, and will be taken to edit_trip.html, where all the previously saved data will be shown with a possibility to modify.
    - A user/owner of a trip can press Delete, and a trip will be deleted, user will be returned to the trips.html. A message will flash "'Username', we've deleted your trip." *Note: Feature to be added to ask a user for confirmation if he/she really wants to delete a trip.*

##### back to [top](#table-of-contents)

5. New Trip screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Confirmed that it won't allow to save a trip with any field empty, shows a message next to such empty field.
    - Confirmed that Choose a ski resort dropdown menu correctly opens a list of ski resorts which are already registered in the database.
    - Dates fields open datepicker, Date-From field does not allow choosing dates before today's. Dates search fields work correctly, once the Date-From is chosen, the datepicker for Date-To shows the chosen Date-From, and does not allow to choose dates before. and vice-versa, when Date-To is chosen first, the datepicker for Date-From will show that date, and won't allow choosing dates after, but also won't let choose dates before today's.
    - Confirmed that Date-To cannot be before Date-from and vice-versa.
    - Adults/Kids fields accepts only numbers from 0, don't allow negative numbers or letters. Shows a message that a correct value should be entered. 
    - Ski/Snowboard shows correct dropdown menu with Ski and Snowboard to choose from. 
    - Pressing Save Trip adds trip to the list of trips, and redirects a user to trips.html, where the list of trips is displayed. Buttons to Edit or Delete a trip are visible only to a user who created that particular trip. 

6. Edit trip screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - All the fields are populated with data previously saved in DB. If i press save without changing anything, all the data is kept as before. Same with pressing Cancel. 
    - If I change any data, and press Save, new data will be saved into DB. 
    - Upon saving a message is flashed "'Username', we've updated your trip."

7. Ski resorts screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Ski resorts are displayed in alphabetical order. 
    - A ski resort card displays its name, a short descriptive title, a thumbnail image, info whether it is a glacier, and if night skiing is possible, link to a ski resort's official website, and Google map link, with additional info field for any useful information about it.
    - Confirmed that both website and map links work and open a target website in another tab. 
    - Search card contains search field, plus Reset & Search buttons. 
    - Putting a name of a ski resort and pressing Search will return a card with a respective ski resort. 
    - If name is not in DB, it will return an empty screen, no ski resorts. 
            *To add a flashed message "Ski Resort is not found*
            *To add a feature to search by an initial/two/three letter/s*
    - Pressing Search with an empty search field, will show a message that the field has to be field. 
    - Pressing Reset will display all the ski resorts in alphabetical order. 

##### back to [top](#table-of-contents)

8. New Ski Resort screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - Confirmed that it won't allow saving with any field empty, except additional info field.
    - Website and map links are validated for an url to be entered. 
    - Glacier and Night skiing dropdown menus show correct choices.
    - Additional info field is not obligatory. 
    - Thumbnail dropdown menu shows correct list of images with names.
    - Pressing Add Ski Resort, saves the info into DB correctly (checked Atlas mongod DB), and takes us to the list of ski resorts in skiresorts.html.
    - Checked add_trip.html, a ski resort is added to the list.
    - Buttons to Edit or Delete a ski resort are visible only to a user who created that particular ski resort. 
    - A user/owner of a ski resort can press Edit, and will be taken to edit_skiresort.html, where all the previously saved data will be shown with a possibility to modify.
    - A user/owner of a ski resort can press Delete, and a ski resort  will be deleted, user will be returned to the ski_resorts.html. A message will flash "'Username', we've deleted your ski resort." *Note: Feature to be added to ask a user for confirmation if he/she really wants to delete a ski resort.*

9. Edit ski resort screen:
    - Has the navbar with all the properly working features/links described above in point 4.
    - All the fields are populated with data previously saved in DB. If i press save without changing anything, all the data is kept as before. Same with pressing Cancel. 
    - If I change any data, and press Save, new data will be saved into DB. 
    - Upon saving a message is flashed "'Username', we've updated your ski resort."

10. Sign Out
    - Pressing take us correctly to the index.html with the main screen with the slogan. The navbar shows only the log and Sign Up & Sing In links. 

##### back to [top](#table-of-contents)

### Testing undertaken in DevTools
The website was tested on all devices available there following the same procedure described in the section above for testing on a laptop, tab & mobile 


### Bugs discovered: 

All the bugs have been moved either to [solved](#solved-bugs) or [unsolved](#unsolved-bugs). 

##### back to [top](#table-of-contents)

#### Solved bugs:

- New user registration:
    * Google message: Passwords are not safe....

- Navbar:
    * Mobile menu: Is not visible, and pressing on menu sandwich does not open menu in mobile view.

- Edit_skiresort.html:
    * Google maps info is lost on opening a specific ski resort to be updated. 
    * Does not show logged-in navbar.

- Edit_trip.html:
    * Name of the stored resort is not posted to the form.

- Trips.html:
    * User's avatar image per trip record is not visible. 
    * User's name is not visible
    * Deleting a trip triggers view distortion. Line of trips become blocks. 

- Trips.html - Search by ski Ski_resorts:
    * User's avatar image per trip record is not visible. 
    * Ski resorts' thumbnails are not visible

- Signing In:
    * Wrong name should redirect to sign_in_page.html. It just flashes the message: Wrong name. Try again. Also shows the full menu, instead of just Sing-In & Sign-Up menu to be visible for non-logged users.

- Add_trip:
    * Does not render trips.html, writes "Collection is not iterble" for {% for trip in trips %}, while a trip is added to the DB correctly

- Ski_resorts.html:
    * Each ski resort displayed multiple times.

- Signing In:
    * Wrong name should redirect to sign_in_page.html. It just flashes the message: Wrong name. Try again. Also shows the full menu, instead of just Sing-In & Sign-Up menu to be visible for non-logged users.

- Add_trip:
    * Does not render trips.html, writes "Collection is not iterble" for {% for trip in trips %}, while a trip is added to the DB correctly

- Edit_skiresort.html:
    * Thumbnail info is lost on opening a specific ski resort to be updated.
    * Skiresort choice is lost on saving, if not chosen again.

- User's profile opened from search for trips:
    * Contact me takes me to UnderConstruction page, if initially I chose some search parameters, and opened a profile from one of the filtered trips, when I press Back button, takes me to a "Re-confirm Submission" warning page, instead of showing a list of trips

##### back to [top](#table-of-contents)

- Sign Up & Sign In on Heroku app:
    * Get this mistake: 'NoneType' object has no attribute 'users'.

- Trips.html, Search:
    * Search does not work in combination: Ski resort name + dates (any of them(from or to) or both)
    * Search does not work with two dates: from & to
    * Dates search fields poorly visible on mobile

- Trips.html, user's profile:
    * User's profile modal brings info of only one user, no matter if a different user's name clicked

- Sign_up.html, Add_skiresort.html:
    * Avatar & thumbnail images/names area of select is too narrow, diaplys is distorted.

- Sign-up form:
    * Where from had same id as calendar datepicker, so was opening datepicker on registration. 

##### back to [top](#table-of-contents)

#### Unsolved bugs:
The bugs below have been left unsolved due to project's time constraints & deadlines; because either the bugs are currently deemed inessential for functionality of the website, or out of capabilities of the developer to resolve them.

- Navbar:
    * Active menu item: shows all of them as active

- Trips.html:
    * If a skiresort is deleted, a skiresort's thumbnail is not displayed on a trip in trips.html.

- Firefox on mobile:
    * Color validation does not work for all fields on Sing Up, popup message is not shown if a field is not filled, but won't let save till all the fields are filled in.

- Edit_trip.html:
    * It is possible to change one date, and set Date-To before Date-From, and save a trip with wrong dates.

- Sign_up_page.html(mobile view, only on Chrome, works ok on Firefox):
    * If i am trying to register with an existing name, flashes a message, the message is covered by the top of the sign-up card.

- Add_skiresort.html, skiresorts.html:
    - Issues with Materialize checkboxes for "spring/autumn/night skiing/glacier" info. Deleted the checkboxes for now. Using strings with "yes/no". If timing will allow, will add checkboxes at the end of the project.
    ** Removed functionality. 

- trips.html(source code html validation):
    - Errors due to repeated ID of users, because one username, in multiple trips created by the user. Plus  repeated ID in See profile link to open a user's profile.
    ** Not fixing because they are not critical, and due to lack of time to re-submit the project for assesment.  

## Further testing: 
1. Asked friends and family to look at the site on their devices & report any issues they found.
