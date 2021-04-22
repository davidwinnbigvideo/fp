<template>
  <div id="app">
    <header>
      <nav>
        <ul>
          <li><router-link to="/"><i class="fas fa-home"></i></router-link></li>
          <li><router-link to="/dashboard"><i class="fas fa-paper-plane"></i></router-link></li>
        </ul>
      </nav>
    </header>
    <router-view />
    <footer id="footer">
      <a href="https://github.com/davidwinnbigvideo/fp"><i class="fas fa-github"></i>Discord 11 hrs</a>
      
    </footer>
  </div>
</template>

<style>
ul {
  position: fixed;
  width: 100%;
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: rgb(204, 0, 0);
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover:not(.active) {
  background-color: rgb(156, 0, 0);
}

.active {
  background-color: #4CAF50;
}

#footer {
  position: fixed;
  padding: 10px 10px 0px 10px;
  bottom: 0;
  width: 100%;
  height: 40px;
}
</style>