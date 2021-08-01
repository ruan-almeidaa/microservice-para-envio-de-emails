## MICROSERVICE PARA ENVIO DE E-MAIL <img alt="gif de e-mail" height="80" src="https://cdn.streamelements.com/uploads/2b04975c-4e9d-4ef7-8973-8008397990ba.gif">
### Tecnologias usadas:
<img alt="java" height="80" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original-wordmark.svg"> 
<img alt="spring" height="80" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original-wordmark.svg">
<img alt="postgresql" height="80" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg">
<img alt="postgresql" height="80" src="https://miro.medium.com/max/1200/1*QOx_tPV5wJnhTzAGhfIiLA.png">

#
O e-mail recebe um **JSON** com:

 - "ownerRef": nome de quem está enviando;
 - "emailFrom": e-mail de quem está enviando;
 - "emailTo":  e-mail que vai receber;
 -  "subject":  o assunto do e-mail;
 -  "text": o texto/corpo do e-mail.
 
<img alt="postgresql" src="https://lh3.googleusercontent.com/AWTB-iS1LYAem3HHCzS2yq7oglUl8-oS65bdT4xFrwKHiq6zWoeZAd7q2i69mS-iXz5k3S-AnzkPE8fZLAGObg9OlxwGau4SFQPBBmHri0GsMQK18GuOvF8fbf1c-Enl-xoowXQWTRCt851dSOKddI-Prdh_XC-XjhqmtZYM8Lp_gXo3EKcXkY50k-JutIFWywfxfcmns237gOfYpghVgLlK65XA2a9j4gI-bTHcOxPnVgHTQgqddv4ICZd2K5PEcbM3NIb-I_6xxmH1-cVP4WcO3CRUejiDoJgsayz6HpGhP_Vwvn1JHbIZA1cP-jbJpqaaQUUrTqe1F1uqW4G8p5pDaTPRwnW-hlNSJlIDubPvMo4ZpJVMhLmj7agGik0bb_Kknett3TLIOIC-vtRhUDI1-_Q1ElAOIKCaY5Ish4flqz5nuYMIdUFR68RVSXMwcvvfMhUdhrxBP-3DQnw2DHp9RkE-bYdXzaJlB4RNgiXpaPyzKrnLvH2hgH4mq8CHSR_-Ftt5rfjZAKoieTkXV7CRbJdm1ucULHhn4CTD5OEYgMEVneGOECADw3ab4B-nwWo787XWK5jb49iDHYn43s4Iu2d6DnNfkGkHUMck3CAFdTOSwP15AUZDX8jl6tf3hxb4o0DQzhuTP7wpmUiImowOcXA96CEgmdOEaStDhQAkOEOwROkSSj0MZghGjMN40o2z6XV0dek3iFowO24U5ls=w1478-h519-no?authuser=0">

A aplicação possui uma classe de enums que controlam as etapas do envio do e-mail, sendo 0 como SENT  e 1 como ERROR, retornando o respectivo status.
<img alt="postgresql" src="https://lh3.googleusercontent.com/w7G3r3myAZ2pFRXk4hZwccuvGKprFo4UU6hBb11yZ94WL8BZNnlA5H-bGBnoS_uT22tcm_dvqtA36c_myBqgC7qn92Nm6kkb3WLGJMXH-aTQ6MfdlAbgz7tRo7j_pDaoZrr-EN-7hP49JevpbnW74C_mPvn-7Pw-HCHTiSlqiwgaqKYkHfqgJRaKwxdbwm3KwtkHZZrdxxXM4eI7miZ2l5xcJ8nYq1JQtK7LjJ3iLj7mkuBY16BWF2p9Fjltg6CQ9JWygOhWT4nXrIITjNLcmuS7WAhDW9kh-Zq0p4H0oGqqukiGVVbRcgzSU3FgxCz-qCbfwrznzy7KElL2oVshB8d5zlj1jNKE6J-9lZ1-qLVOC9xF5KtI_vRyieKt2jzHKVaf4-qRLUiUcDkRL8q6zf-eceLgoLQeRq2WLOZWsTYHekBe7kJnklRsZrUnQNB-nerUjNtzF5Fx3dHvgS2-weC9ReLrlIQG9gsgPIqhjR5evqIDHypAF21LLhZbxzKW6aOcy1KyFCg8SMQ4-NkOXlZhiaauHbYvSCm5da6Nb7UzMP1jnJiXY2DDzIdZzY2J1LzYWtMo9jGxlj5gx6GDv0tEmN2CRGKA-9Jd8EnKd5ELXf7uvMn5a30IHAcPGd8cHYgWrqDLnXqE66OhBJgVo-tFnA0hFBZxbjddqmRfwvfzZM32T8-jTgURIB-jtAb5lzGSiS8uIttHNbDwsb3niFU=w1472-h380-no?authuser=0">

Este é o resultado no banco de dados:
<img alt="postgresql" src="https://lh3.googleusercontent.com/uWMeDDmQQIy3NeAm6TKTatdR5ajgYmnd5s-95YzQzAJYUHP2SpTn2hPh6wf-Hir0oxJt0Dmr8D45JR0y_u0WD7ODdK1-Qns417MvhYFWjLumVDR8zREFojZR8DFpkwLpu41JRjlFnEzCQQ2cb8G0m3an9nlf_TSEH7jGr6Kh3TPEzh7WQqhkAGOpHVXFm6Ni_IcjyBmPDcHMSeLewQFZxJi__lzq2g-4dbcvtPJJV-nWIg6kvHrwivoEbErY1YnqK4pIXsFY7CiqUHpJpXFwh33bbUX2TFTdhL6H5zBemCN0DbkJvikwGdH1o7uq-wz3JdrhG1q9HrZoCRj2iAoA7MFcZ6QxpoOIf7-VzExAfjNMgAv2msxLo_Jb8TuHSnsm-mOc6KnQvz_35j4KY3hOu6SWN3610I0tBgGKdFO8_sfae39YA9nPiG8LmbM5j2H7JptGUqKTiS0sWEZ023vlPBV6hFov3Kbbmovm32aBRfygOJHZGZcSck8ICly0w3ShZE7cOWUoT7zqwwhIobpbvhma-x_rtudsSJEPZXbB1y-oJG-y783rTG-GwNJB3SbiwTN0Ip-F41OD8lxfbBOE8mrNrIkVcYd0dX5IeF2kIkhiV-C0N56dIum5V2UIousqWiYdb2ymeF1vUQ-gVC3mLWOARbCKlcLPuQCMca5WZzyS_ojVREHoVVueA7W-rvr0StmhJMMWYKcLCssy95xjFHI=w1609-h274-no?authuser=0">

E na caixa de e-mail:
<img alt="postgresql" src="https://lh3.googleusercontent.com/VqHaPSALOvz0bJzMzBkfOL2DBIb2odNbyZfNMqGqiahptKdo3PNTnqs_E32H6SE7zdwP9pfUN8kdf5vOzcku3-iSJlm-ZF1KciiRjD1CzOwAB0bb77geH4LrOo_I5m6iUyInpRj8Y71xVS0xsKvN5NM_xji2fxzfo2M0k_4hYVF9yPkKxnfQj9Yu1vJlS_h-5GUSqyJQWKaZnsojL56VsD5J7YR7QL2j06hK93ojBokn5giS4AMR6_8cJklnkoE6KCjovYvDW2OwP9aiYFVIiZ-B2EBqoY3J4ErpfNvVCn0xxJAaMECBteEM-LGMhfYx5cpVnffTFz-HkVvah7jfkWP5nS7gxGkRwqCBDvKT4_WsOijtNRPvMJvcdub_Leb95iiLzHKlQvjgU3H5R7su3c3CuqORJ6YlCTmFy7YusPA0-Gd8f4A8k_8UmEe9kXHqmqmEMc322atSTX515RzZjckbN2H5XXNZP9Y4eL-uEMDRYjfy3f-gV7ZZ1eyP-dmXTcPJue-WrCoYC-Yat7bqo9_FDeMiisbu0ZDrQDk5WBpkgweY1w4z_Mva24fbXOyjAK27runAvQVzA3i2oNBL_r5zXdmw3BE2Ld0WFkmCyNhd4alGNzuJMq4oKiMnQutBG6mgDWY3h95NPlPhgFssgSL-Jj6y7kOf1P5xxnpuJeH2mrVYwikDvPGVUzlB7JZNBKNqBy84SqEu2aXGwxrYbbA=w1775-h396-no?authuser=0">

