# @suenot/send-mail

0. The package wraps the npm-package [nodemailer](https://nodemailer.com/)
1. Prerequisites: an account on [gmail](https://gmail.com/) with an [App Password](https://knowledge.workspace.google.com/kb/how-to-generate-an-app-passwords-000009237)
    1. In case the App password option is missing in the account management panel after enabling two-factor authentication, try opening the [direct link](https://security.google.com/settings/security/apppasswords)
2. Mail client setup:
    1. Create a `TransporterUser` object, in the value specify the email address
    2. Create a `TransporterPass` object, in the value specify the App Password
    3. Create a `TransporterService` object, in the value specify `gmail`
3. Preparing the message:
    1. Create a `LetterSubject` object, in the value specify the subject of the letter
    2. Create a `LetterText` object, in the value specify the text of the letter
    3. Create a `SendTo` object, in the value specify the email address of the recipient
4. To send a letter, create a `SendEmail` object from an instance of the `LetterSubject` object to an instance of the `SendTo` object.
