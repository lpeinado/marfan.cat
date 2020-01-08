<template>
  <Layout>
    <h1>Qui som?</h1>
    <figure>
      <g-image src="~/assets/qui_som.jpg" width="500" class="main-img"/>
    </figure>
    
    <p>
      Els afectats per la Síndrome de Marfan a Catalunya fa anys que ens hem associat i vam crear aquesta agrupació per tal de millorar
      la nostra qualitat de vida i compartir tota la informació necessària per tirar endevant. 
    </p>
    <p>
      La Síndrome de Marfan és una malaltia minoritària i ens cal estar units i compartir tots els coneixements que anem acumulant
      per tal de fer-nos costat els uns als altres.
    </p>
    <p>La raó de ser de l'Associació a Catalunya és treballar en la sensibilització vers la Síndrome de Marfan a
      nivell local i oferir una ajuda propera als afectats.
    </p>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Qui som?'
  }
}
</script>

<style>
.main-img{
  transition: width 2s ease;
}
.main-img:hover {
  width: 700px;
}
</style>
