<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img src="https://entrepreneo.fr/img/2016/01/entrepreneur-auto-manager_l.jpg" style="max-width: 100%;">
    <h2>Génération</h2>
    <ul>
      <li>
        <a class="undevelopped"
          href="https://vuejs.org"
          target="_blank"
        >
        Projet avec les infos de bases
        </a>
      </li>
      <li>
        <a class="undevelopped"
          href="https://forum.vuejs.org"
          target="_blank"
        >
        Fiches clients
        </a>
      </li>
      <li>
        <a class="undevelopped"
          href="https://chat.vuejs.org"
          target="_blank"
        >
        PDF de devis / factures
        </a>
      </li>
      <li>
        <a class="undevelopped"
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Module de gestion de temps
        </a>
      </li>
      <br>
      <li>
        <a class="undevelopped"
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
        Livre de recettes / achats
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: "Bienvenue sur DVCI - Entrepreneur Tool"
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
