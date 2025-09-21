---
layout: page
title: "Authentizierung zum Privatbereich"
permalink: /privat/
---

<script>
  function Anmelden () {
    let Passwort = 'fam-chiarcos.1234';
    let Eingabe = window.prompt('Passwort erforderlich');

    if (Eingabe != Passwort) {
        alert('Passwort ist Falsch!');
    } else {
        document.cookie = 'fam-chiarcos.1234'
        location.href = '/privat/open';
    }
    
  }
  function CookieLogIn () {
    if (document.cookie == 'fam-chiarcos.1234'){
      location.href = '/privat/open/'
    }
    else {
      alert('Sie haben sich noch nicht angemeldet.')
    
  }
</script>

# Der Privatbereich

<input type="button" value="Anmelden" onclick="Anmelden()"/><br>
<input type="button" value="Letzte Anmeldedaten verwenden" onclick="CookieLogIn()"/>
