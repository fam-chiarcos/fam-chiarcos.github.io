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
      fensterOeffnen();
    }
  }
    
  
  
  function CookieLogIn () {
    if (document.cookie == 'logout') {
      alert('Sie sind nicht Eingeloggt');
    }
    else if (document.cookie == 'fam-chiarcos.1234'){
      fensterOeffnen();
    }
    else {
      alert('Sie sind nicht Eingeloggt');
    }
    
  }
function fensterOeffnen () { 
  var MeinFenster = window.open("about:blank", "Zweitfenster", "width=300,height=400,left=100,top=200"); 
  MeinFenster.location.href="/privat/open" 
  MeinFenster.focus(); 
}

</script>

# Der Privatbereich

<input type="button" value="Einloggen" onclick="Anmelden()"/><br>
<input type="button" value="Anmelden als Familie Chiarcos" onclick="CookieLogIn()"/> Achtung: Nicht alle Geräte unterstützen diese Option<br>
<input type="button" value="Abmelden" onclick="document.cookie = 'logout'; alert('Familie Chiarcos ist abgemeldet.')"/>
