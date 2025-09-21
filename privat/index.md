---
layout: page
title: "Authentizierung zum Privatbereich"
permalink: /privat/
---

<script>
  function Anmelden () {
    let Passwort = 'fam-chiarcos.1234';
    let Eingabe = window.prompt('Geben sie das Passwort für das Benutzerkonto "Famile Chiarcos" ein.');

    if (Eingabe != Passwort) {
      alert('Passwort ist Falsch!');
    }
    else {
      document.cookie = Eingabe
      location.href = '/privat/open';
    }
  }
    
  
  
  function CookieLogIn () {
    if (document.cookie == 'logout') {
      alert('Sie sind nicht Eingeloggt');
    }
    else if (document.cookie == 'fam-chiarcos.1234'){
      location.href = '/privat/open/';
    }
    else {
      alert('Sie sind nicht Eingeloggt');
    }
    
  }
</script>

# Der Privatbereich

<input type="button" value="Einloggen" onclick="Anmelden()"/><br>
<input type="button" value="Anmelden als Familie Chiarcos" onclick="CookieLogIn()"/> Achtung: Nicht alle Geräte unterstützen diese Option<br>
<input type="button" value="Abmelden" onclick="document.cookies = 'logout'; alert('Familie Chiarcos ist abgemeldet.')"/>
