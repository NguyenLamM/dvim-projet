<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img src="https://entrepreneo.fr/img/2016/01/entrepreneur-auto-manager_l.jpg" style="max-width: 100%;">
    <div style="display:flex; flex-direction: row; align-items: center">
    <div ref='content' style="width: 100%;">
      <h1>Créer une fiche Client: </h1>
      <label for="ename">Nom Entreprise :</label>
      <input type="text" id="ename" name="ename"><br><br>
      <label for="fname">Prénom :</label>
      <input type="text" id="fname" name="fname"><br><br>
      <label for="lname">Nom de famille :</label>
      <input type="text" id="lname" name="lname"><br><br>
      <label for="email">Email :</label>
      <input type="text" id="email" name="email"><br><br>
      <label for="adresse">Adresse :</label>
      <input type="text" id="adresse" name="adresse"><br><br>
      <label for="pays">Pays :</label>
      <input type="text" id="pays" name="pays"><br><br>
      <label for="postale">Code Postale :</label>
      <input type="text" id="postale" name="postale"><br><br>
      <button @click="downloadclient">Télécharger la fiche client</button>
    </div>
    <div ref='content' style="width: 100%;">
      <h1>Créer une fiche Projet: </h1>
      <label for="pname">Nom Projet :</label>
      <input type="text" id="pname" name="pname"><br><br>
      <label for="description">Description :</label>
      <input type="text" id="description" name="description"><br><br>
      <label for="investissement">Investissement estimé :</label>
      <input type="text" id="investissement" name="investissement"><br><br>
      <label for="temps">Temps de réalisation :</label>
      <input type="text" id="temps" name="temps"><br><br>
      <label for="adressep">Adresse :</label>
      <input type="text" id="adressep" name="adressep"><br><br>
      <label for="paysp">Pays :</label>
      <input type="text" id="paysp" name="paysp"><br><br>
      <button @click="download">Télécharger la fiche projet</button>
    </div>
    </div>
  </div>
</template>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.5.1/jspdf.debug.js" integrity="sha384-THVO/sM0mFD9h7dfSndI6TS0PgAGavwKvB5hAxRRvc0o9cPLohB0wb/PTA7LdUHs" crossorigin="anonymous"></script>
<script>
import jsPDF from 'jspdf'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: "Bienvenue sur DVCI - Entrepreneur Tool"
    }
  },
  methods:{
    downloadclient(){
    var doc = new jsPDF()
    doc.text("FICHE CLIENT",70,20)
    doc.text("Entreprise :" + document.getElementById("ename").value,50,40)
    doc.text("Prénom client :" + document.getElementById("fname").value,50,50)
    doc.text("Nom client :" + document.getElementById("lname").value,50,60)
    doc.text("Email  :" + document.getElementById("email").value,50,70)
    doc.text("Adresse :" + document.getElementById("lname").value,50,80)
    doc.text("Pays :" + document.getElementById("pays").value,50,90)
    doc.text("Code postale :" + document.getElementById("postale").value,50,100)
    doc.save(document.getElementById("ename").value + '.pdf')
    },
    download(){
    var doc = new jsPDF()
    doc.text("Fiche PROJET",70,20)
    doc.text("Nom du projet :" + document.getElementById("pname").value,50,40)
    doc.text("Description :" + document.getElementById("description").value,50,50)
    doc.text("Investissement :" + document.getElementById("investissement").value,50,60)
    doc.text("Adresse :" + document.getElementById("temps").value,50,80)
    doc.text("Pays :" + document.getElementById("paysp").value,50,90)
    doc.text("Code postale :" + document.getElementById("adressep").value,50,100)
    doc.save(document.getElementById("pname").value + '.pdf')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.developped {
  color: green;
}
.undevelopped{
  color: red;
}
</style>
