<div>

## MICROSERVICE PARA ENVIO DE E-MAIL <img alt="gif de e-mail" height="80" src="https://cdn.streamelements.com/uploads/2b04975c-4e9d-4ef7-8973-8008397990ba.gif">
### Tecnologias usadas:
<img alt="java" height="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original-wordmark.svg"> 
<img alt="spring" height="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original-wordmark.svg">
<img alt="postgresql" height="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg">
<img alt="postgresql" height="50" src="https://miro.medium.com/max/1200/1*QOx_tPV5wJnhTzAGhfIiLA.png">
</div>

#
O e-mail recebe um **JSON** com:

 - "ownerRef": nome de quem está enviando;
 - "emailFrom": e-mail de quem está enviando;
 - "emailTo":  e-mail que vai receber;
 -  "subject":  o assunto do e-mail;
 -  "text": o texto/corpo do e-mail.
 
<img alt="json" src="https://github.com/ruan-almeidaa/microservice-para-envio-de-emails/blob/main/images/postman.png?raw=true">

A aplicação possui uma classe de enums que controlam as etapas do envio do e-mail, sendo 0 como SENT  e 1 como ERROR, retornando o respectivo status.
<img alt="enum" src="https://github.com/ruan-almeidaa/microservice-para-envio-de-emails/blob/main/images/postaman%20enviado.png?raw=true">

Este é o resultado no banco de dados:
<img alt="banco de dados" src="https://github.com/ruan-almeidaa/microservice-para-envio-de-emails/blob/main/images/banco%20de%20dados.png?raw=true">

E na caixa de e-mail:
<img alt="e-mail" src="https://github.com/ruan-almeidaa/microservice-para-envio-de-emails/blob/main/images/caixa%20de%20e-mail.png?raw=true">
