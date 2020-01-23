<p align="center">
  <a href="https://userbase.com"><img src="docs/logo.png" width="441" alt="Userbase"></a>
</p>

<p align="center">
<b>Create secure and private web apps using only static JavaScript, HTML, and CSS.</b>
</p>

## What is Userbase?

Userbase is the easiest way to add user accounts and user data persistence to a static website. All Userbase features are accessible through a very simple JavaScript SDK, directly from the browser. No backend necessary.

### Built-in user accounts
Userbase takes care of your user accounts. The Userbase SDK lets you sign up, login, and logout users directly from your static website, and the Userbase Admin panel lets you manage all your registered users from one place.

### Zero-management database
Instead of sending database queries to a server, Userbase sends all the user's data to the browser. Queries happen client-side, and there is nothing on the backend to manage or worry about.

### End-to-end encryption
Userbase won't show you what your users store in your web app. Userbase spares you from the liability of handling user data by encrypting all database operations in the user's browser.

## When would I use it?
If you're building a web app, you will likely need a database and a backend. Userbase can replace both of those things...

- If you want to build a web app without writing any backend code.
- If you never want to see your users' data.
- If you're tired of dealing with databases.
- If you want to radically simplify your GDPR compliance.
- And if you want to keep things really simple.

## How do I start?
Userbase will become available on January 25th, 2020. You can [subscribe to the mailing list](https://userbase.com/mailing-list) to receive important updates in your inbox.

## Development

### Configure the AWS credentials
Running the Userbase server requires an AWS account. You just need to provide your AWS credentials and the server will automatically create all the AWS resources it needs. To run the app locally, simply put your AWS credentials in `~/.aws/credentials` under a profile called `encrypted`:

```
echo "
[encrypted]
aws_access_key_id=<YOUR ACCESS KEY>
aws_secret_access_key=<YOUR SECRET KEY>" >> ~/.aws/credentials
```

### Check out the repo

```
git clone https://github.com/encrypted-dev/userbase.git
```

### Install the dependencies

#### Mac/Linux
```
npm install
```

#### Windows WSL

To bypass symlink issues on Windows, you need to disable symlinks on WSL. For more info, check WSL issues [#14](https://github.com/Microsoft/WSL/issues/14) and [#26](https://github.com/MicrosoftDocs/WSL/issues/26).

```
npm install --no-bin-links
```

### Start the dev server

```
npm start
```

Go to http://localhost:3000 and you should see the sign in screen.

### Running tests
We use [Cypress](https://www.cypress.io/) to run tests, all the test files are under the ./cypress dir.

```
npm run test
```

## License

This project is released under the [MIT License](LICENSE).
