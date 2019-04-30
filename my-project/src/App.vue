<template>
  <div class="project">
    <div class="title">
      <img class="image" src="./assets/Titelbild.png" alt="Schwangerschaft">
      <h1>Unser tolles Projekt + Bild</h1>
        <div class="title-content">
          <p>Hier Text, Einleitung etc.</p>
        </div>
      </div>
      <div class="content-white">
        <p><b>Hier Inhalt einfügen / Schwangerschaftsabbrüche</b>
        <br>und tolle Diagramme, Link Schwangerschaftsabrüche: https://www.destatis.de/DE/Themen/Gesellschaft-Umwelt/Gesundheit/Schwangerschaftsabbrueche/Tabellen/rechtliche-begruendung.html</p>
      </div>  
      <div class="content-grey">
        <p><b>Hier Inhalt einfügen / Entbindungen</b>
        <br>und tolle Diagramme, Link Entbindungen: https://www.destatis.de/DE/Themen/Gesellschaft-Umwelt/Gesundheit/Krankenhaeuser/Tabellen/krankenhausentbindungen-kaiserschnitt.html</p>
      </div>
      <div class="content-white">
        <p><b>Hier Inhalt einfügen</b>
        <br>und tolle Diagramme / zeiträume / Grafik</p>
      </div> 
      <div class="footer">
        <p>Ein Projekt von Grit Ludwig, Anne Westphal & Anna Tarrach</p>
      </div>
  </div>

</template>

<script>
export default {
  
}
</script>


<style>
  html, body {
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }
  .project {
    color: rgb(26, 26, 26);
  }
  .title {
    text-align: center;
    background-color:rgb(216, 238, 238);
    padding: 30px;
  }
  .image {
    width:70%;
  }
  .content-white {
    background-color: white;
    padding: 30px;

  }
  .content-grey {
    background-color:rgb(240, 240, 240);
    padding: 30px;
  }
  .footer {
    font-size: 8pt;
    color:rgb(107, 107, 107);
    text-align:center;
    padding: 30px;
  }
</style>
