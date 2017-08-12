<html>

<head>
    <meta charset="utf-8" />
    <title>Messages</title>
    <link rel="stylesheet" type="text/css" href="messages.css" />
    <script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
    <script src="app.js"></script>
</head>

<body onload="startApp()">

<div id="app">
    <header id="menu">
        <a href="#" class="anonymous" id="linkMenuAppHome">Home</a>
        <a href="#" class="anonymous" id="linkMenuLogin">Login</a>
        <a href="#" class="anonymous" id="linkMenuRegister">Register</a>

        <a href="#" class="useronly" id="linkMenuUserHome">Home</a>
        <a href="#" class="useronly" id="linkMenuMyMessages">My Messages</a>
        <a href="#" class="useronly" id="linkMenuArchiveSent">Archive (Sent)</a>
        <a href="#" class="useronly" id="linkMenuSendMessage">Send Message</a>
        <a href="#" class="useronly" id="linkMenuLogout">Logout</a>

        <span class="useronly" id="spanMenuLoggedInUser">Welcome, {user}!</span>
    </header>

    <main>
        <div id="loadingBox">Loading ...</div>

        <div id="infoBox">Info</div>

        <div id="errorBox">Error</div>

        <section id="viewAppHome">
            <h1>Welcome</h1>
            Welcome to our messaging system.
        </section>

        <section id="viewLogin">
            <h1>Please login</h1>
            <form id="formLogin">
                <label>
                    <div>Username:</div>
                    <input type="text" name="username" id="loginUsername" required />
                </label>
                <label>
                    <div>Password:</div>
                    <input type="password" name="password" id="loginPasswd" required />
                </label>
                <div>
                    <input type="submit" value="Login" />
                </div>
            </form>
        </section>

        <section id="viewRegister">
            <h1>Please register here</h1>
            <form id="formRegister">
                <label>
                    <div>Username:</div>
                    <input type="text" name="username" id="registerUsername" required />
                </label>
                <label>
                    <div>Password:</div>
                    <input type="password" name="password" id="registerPasswd" required />
                </label>
                <label>
                    <div>Name:</div>
                    <input type="text" name="name" id="registerName" />
                </label>
                <div>
                    <input type="submit" value="Register" />
                </div>
            </form>
        </section>

        <section id="viewUserHome">
            <h1 id="viewUserHomeHeading">Welcome, {user}!</h1>
            <a href="#" id="linkUserHomeMyMessages">My Messages</a>
            <a href="#" id="linkUserHomeSendMessage">Send Message</a>
            <a href="#" id="linkUserHomeArchiveSent">Archive (Sent)</a>
        </section>

        <section id="viewMyMessages">
            <h1>My Messages</h1>
            <div class="messages" id="myMessages">
            </div>
        </section>

        <section id="viewArchiveSent">
            <h1>Archive (Sent Messages)</h1>
            <div class="messages" id="sentMessages">

            </div>
        </section>

        <section id="viewSendMessage">
            <h1>Send Message</h1>
            <form id="formSendMessage">
                <div>Recipient:</div>
                <div>
                    <select name="recipient" required id="msgRecipientUsername">
                        <option value="maria">Maria Georgieva (maria)</option>
                        <option value="guest">guest</option>
                        <option value="peter">Peter Ivanova (peter)</option>
                        <option value="todor">todor</option>
                        <!-- TODO: more users will come here -->
                    </select>
                </div>
                <div>Message Text:</div>
                <div><input type="text" name="text" required id="msgText" /></div>
                <div><input type="submit" value="Send" /></div>
            </form>
        </section>
    </main>

    <footer>Messaging System - Simple SPA Application</footer>
</div>

</body>

</html>
