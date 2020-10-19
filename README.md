# Spring Boot + Ember.js

# Running
http://localhost:8080

# Rebuilding
docker-compose up --build

# Notes

# docker-compose.yml 
* Nginx generalno nije potreban u ovom setupu. Mozes direktno mapirati 8080:4200 za client
* dockerfile = Dockerfile je default name pa ne mora da se navodi osim ako se ne zove drugacije
* stdin_open: true Ovo ti ne treba jer ti svakako streamuju logove kad uradis docker-compose up na stdout tako da je prakticno neuporebljivo :D

# server/Dockerfile
* Kapiram da si koristila lokalni maven ili preko docker run commande posto ne vidim da ga instaliras ovde niti da ovaj image ima maven, a nema ni build koraka uopste - Pogledaj primer kako radi multistage build i kroz Dockerfile da buildujes binary
* u tvom Dockerfile su podrazumeva da vec imas izbildan binary lokalno i da ga samo kopiras u image.
* Pogledaj deo i kako keshira dependencies koje skida da ne mora iznova (taj generalno problem nemas ako koristis lokalni maven ali ako bilo ko skine repo kao ja nece moci samo da pokrene docker-compose up i da mu sve radi jer nema buildovan binary)

# Generalno si super uradila i lepo si se snasla :)
