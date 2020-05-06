Develop
    Config (folder)
        Middleware (folder)
            isAuthenticated.js : this file allows us to know if the user in logged in and if not, they are restriced to the login page. in other words, the authentication of each user. 
        config.json : sets up different enviroments like the test and production
        passport.js : this file brings in all the passport library tools. it sets the logic for the varification for the userinputs. for example we want to use their email as their username. it then uses that info to check against the database. if the email doesn't exist, alerts are sent to the user. 
    Models (folder)
        index.js : 
        user.js : this file creates the user db. it is then exported to be used in other parts of the app. it is also bringing in bcrypt lib.  
    Public (folder)
        js (folder)
            login.js : contains the logic and javascript that renders html for the login.html page. this file takes in user input and posts the info the the /api/login route. then it takes them to the /members page.  
            members.js : contains the logic and javascript that renders html for the members.html page. this page displays the current logged-in. it then displays their email on the page. 
            signup.js : contains the logic and javascript that renders html for the signup.html page. this file takes in user input and posts the info the the /api/signup route. then it takes them to the /members page.  
        stylesheets(folder)
            style.css : contains all of the css for the app/pages
        login.html : This file contains all the front-end container html that is dependent on what is created in the login.js file. 
        members.html : This file contains all the front-end container html that is dependent on what is created in the member.js file.
        signup.html : This file contains all the front-end container html that is dependent on what is created in the signup.js file.
    Routes (folder)
        api-routes.js : the is file uses the models and passport files (db and passport respectfully). this sets up all the routes assositated with the signup and login pages. here you will know where to find specific data. 
        html-routes.js : this page brings in the path library.  it tells the browser what to display (html) to the user. for example, if the user who already has an account, you would want them to be directed to the memebers page. 
    Package.json : dependencies are outlines here. this is what is installed in npm i is run. 
    server.js : sets up the port and syncs the models. creates the express app and brings in passport (username/password) and starts the session for the user. 

