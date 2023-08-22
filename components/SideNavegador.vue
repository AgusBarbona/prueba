<template>
    <div class="sidenav" :class="{ 'open': isOpen }">
      <button @click="toggleNav">Cerrar</button>
      <ul>
        <li>Inicio</li>
        <li>Matchs</li>
        <li>Chats</li>
        <li>Búsqueda</li>
        <li>Mi Cuenta</li>
        <li>Soporte</li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isOpen: false
      }
    },
    methods: {
      toggleNav() {
        this.isOpen = !this.isOpen;
      }
    }
  }
  </script>
  
  <style scoped>
  .sidenav {
    position: fixed;
    top: 0;
    left: -250px;
    width: 250px;
    height: 100%;
    background-color: #111;
    overflow-x: hidden;
    transition: 0.5s;
    padding-top: 60px;
  }
  
  .sidenav ul {
    list-style-type: none;
    padding: 0;
  }
  
  .sidenav ul li {
    padding: 10px 15px;
    color: white;
    cursor: pointer;
  }
  
  .sidenav ul li:hover {
    background-color: #575757;
  }
  
  .sidenav.open {
    left: 0;
  }
  </style>
  