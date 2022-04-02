<!-- Header.vue -->
<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#">L-VUE</a>
        <button
            class="navbar-toggler"
            type="button"
            data-toggle="collapse"
            data-target="#navbarNavAltMarkup"
            aria-controls="navbarNavAltMarkup"
            aria-expanded="false"
            aria-label="Toggle navigation"
        >
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
            <div class="navbar-nav">
                <router-link to="/" class="nav-link" exact>
                    <i class="fas fa-fw fa-tachometer-alt"></i>
                    <span>Dashboard</span>
                </router-link>
                <li class="nav-item">
                    <router-link to="/categories" class="nav-link" exact>
                        <i class="fas fa-fw fa-chart-area"></i>
                        <span>Categories</span>
                    </router-link>
                </li>
                <a class="nav-item nav-link" href="#">Features</a>
                <a class="nav-item nav-link" href="#" onclick="event.preventDefault(); document.getElementById('logout-form').submit();">Logout</a>
                

<form id="logout-form" action="logout" method="POST"
                                        class="d-none">
                                        <input type="hidden" name="_token" :value="csrf">
                                    </form>

            </div>
        </div>
    </nav>
</template>

<script>

export default {
 data() {
   return {
     csrf: document.querySelector('meta[name="csrf-token"]').getAttribute('content')
   }
 },
 methods: {
   submit : function(){
     this.$refs.form.submit();
   }
 }
}

</script>
