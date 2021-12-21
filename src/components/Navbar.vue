<template>
  <nav class="site-nav navbar navbar-expand bg-primary navbar-dark">
    <div class="container-fluid">
      <router-link to="/" class="navbar-brand">Home</router-link>
      <div class="navbar-nav ml-auto">
        <router-link to="/meetings" class="nav-item nav-link"
          >meetings</router-link
        >
        <router-link to="/login" class="nav-item nav-link">login</router-link>
        <router-link to="/register" class="nav-item nav-link"
          >register</router-link
        >
      </div>
    </div>
  </nav>
</template>