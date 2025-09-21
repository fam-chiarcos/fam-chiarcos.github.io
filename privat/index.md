---
layout: page
title: "Authentizierung zum Privatbereich"
permalink: /privat/
---

<script>
  function Anmelden () {
    let Passwort = 'fam-chiarcos.1234';
    if (document.cookie == 'fam-chiarcos.1234'){
      location.href = '/privat/open/'
    }
    else {
      False ()
    }
    
  }

  function False ():
    
      let Eingabe = window.prompt('Passwort erforderlich');
      
      if (Eingabe != Passwort) {
          alert('Passwort ist Falsch!');
          document.cookie = Eingabe
      }
      else {
          document.cookie = Eingabe
          location.href = '/privat/open';
      }


    
  }
</script>

# Der Privatbereich

<input type="button" value="Anmelden" onclick="Anmelden()"/><br>
