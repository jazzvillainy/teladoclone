<template>
  <footer class="footer">
    <div class="content has-text-centered">
      <nav class="level">
        <p>© 2002-2024 Teladoc, Inc. All rights reserved.</p>
        <div class="level-item has-text-centered">
          <a class="link" href="#"> Terms of Service </a>
        </div>
        <div class="level-item has-text-centered">
          <a class="link" href="#"> Notice of Privacy Practices </a>
        </div>
        <div class="level-item has-text-centered">
          <a class="link" href="#">
            Notice of Non-Discrimination and Language Assistance
          </a>
        </div>
      </nav>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
/* *{

    border:solid;
} */
p {
  font-size: 13px;
  font-style: normal;
  font-weight: 400;
  line-height: 20px;
  color: #727069;
  width: fit-content;
}
nav {
  display: flex;
  width: 100%;
  justify-content: space-between;
}
.content {
  display: flex;
}
a {
  text-decoration: none;
}
.has-text-centered {
  align-content: center;
}
footer {
  /* scale: ; */
  width: 80%;
  border-top: 2px dotted;
  margin: 0% 5% auto;
  padding-left: 2%;
  padding-right: 3%;
  padding-top:1%;
  color: #727069;
  
}
</style>
