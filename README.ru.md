# @suenot/mail-sender

### Инструкция
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


### Видео использования
https://youtu.be/wQq--zyYqr8

### Скриншоты
![330236631-03f9cdaf-4cc3-4cd0-a3ef-5ef4c4a083c7](https://github.com/suenot/deep-mail-sender/assets/1426876/bb8f42b4-b039-44b2-a4a3-84c5efc856f0)

![photo_2024-05-14 03 08 06](https://github.com/suenot/deep-mail-sender/assets/1426876/11480509-aabd-4c99-ba93-eabf27f3f30a)
