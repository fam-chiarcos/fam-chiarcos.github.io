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
        location.href = '/privat/open';
    }
  }
</script>

# Der Privatbereich

<input type="button" value="Anmelden" onclick="Anmelden()"/>
