# @suenot/send-mail

0. Пакет оборачивает npm-package [nodemailer](https://nodemailer.com/)
1. Пререквизиты: аккаунт на [gmail](https://gmail.com/) с [App Password](https://knowledge.workspace.google.com/kb/how-to-generate-an-app-passwords-000009237)
  1. В случае отсутсвия опции App password в панели управления аккаунтом после включения двухфакторной аутентификации попробуйте просто открыть [прямую ссылку](https://security.google.com/settings/security/apppasswords)
2. Настройка почтового клиента
  1. Создайте связь `TransporterUser`, в значении укажите адрес электронной почты
  2. Создайте связь `TransporterPass`, в значении укажите App Password
  3. Создайте связь `TransporterService`, в значении укажите `gmail`
3. Подготовка сообщения
  1. Создайте связь `LetterSubject`, в значении укажите тему письма
  2. Создайте связь `LetterText`, в значении укажите текст письма
  3. Создайте связь `SendTo`, в значении адрес электронной почты получателя
4. Чтобы отправить письмо создайте связь `SendEmail` от экземпляря связи `LetterSubject` к экземпляру связи `SendTo`
