# @suenot/mail-sender

- Пакет оборачивает npm-package [nodemailer](https://nodemailer.com/)
- Пререквизиты: аккаунт на [gmail](https://gmail.com/) с [App Password](https://knowledge.workspace.google.com/kb/how-to-generate-an-app-passwords-000009237)
  - В случае отсутсвия опции App password в панели управления аккаунтом после включения двухфакторной аутентификации попробуйте просто открыть [прямую ссылку](https://security.google.com/settings/security/apppasswords)
- Настройка почтового клиента
  - Создайте связь `TransporterUser`, в значении укажите адрес электронной почты
  - Создайте связь `TransporterPass`, в значении укажите App Password
  - Создайте связь `TransporterService`, в значении укажите `gmail`
- Подготовка сообщения
  - Создайте связь `LetterSubject`, в значении укажите тему письма
  - Создайте связь `LetterText`, в значении укажите текст письма
  - Создайте связь `SendTo`, в значении адрес электронной почты получателя
- Чтобы отправить письмо создайте связь `SendEmail` от экземпляря связи `LetterSubject` к экземпляру связи `SendTo`
