<template>
    <div class="container pt-3">
        <nav class="navbar" role="navigation" aria-label="main navigation">
            <div class="navbar-brand">
                <a class="navbar-item">
                    <img src="http://shreethemes.in/cristino/layouts/images/logo-light.png"  height="16">
                </a>

                <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                    <span aria-hidden="true"></span>
                </a>
            </div>
            <div id="navbarBasicExample" class="navbar-menu">
                <div class="navbar-start">
                    <a class="navbar-item">
                        Home
                    </a>

                    <a class="navbar-item">
                        Services
                    </a>
                    <a class="navbar-item">
                        Resume
                    </a>
                    <a class="navbar-item">
                        Projects
                    </a>
                    <a class="navbar-item">
                        Blog
                    </a>
                    <a class="navbar-item">
                        Contact
                    </a>
                    <div class="navbar-item has-dropdown is-hoverable">
                        <a class="navbar-link">
                        Pages
                        </a>

                        <div class="navbar-dropdown">
                            <a class="navbar-item">
                                Blog
                            </a>
                            <a class="navbar-item">
                                Portfolio
                            </a>
                        </div>
                    </div>
                    <div class="ml-6">
                        <a class="button social">
                            <span class="icon">
                                <i class="fab fa-facebook-f"></i>
                            </span>
                        </a>
                        <a class="button social">
                            <span class="icon">
                                <i class="fab fa-twitter"></i>
                            </span>
                        </a>
                        <a class="button social">
                            <span class="icon">
                                <i class="fab fa-instagram"></i>
                            </span>
                        </a>
                    </div>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
    .navbar {
        background-color: transparent;
    }

    .navbar-item, .navbar-link {
        color: #fff;
        text-transform: uppercase;
        font-family: 'Montserrat', sans-serif;
        font-size: 11px;
        font-weight: 600;
    }
    a.navbar-item:focus, a.navbar-item:focus-within, a.navbar-item:hover, a.navbar-item.is-active, .navbar-link:focus, .navbar-link:focus-within, .navbar-link:hover, .navbar-link.is-active {
        background-color: transparent;
        color: #e54b4b;
    }
    .navbar-item.has-dropdown:focus .navbar-link, .navbar-item.has-dropdown:hover .navbar-link, .navbar-item.has-dropdown.is-active .navbar-link {
        background-color: transparent;
    }
    .navbar-dropdown a.navbar-item:focus, .navbar-dropdown a.navbar-item:hover {
        background-color: whitesmoke;
        color: #0a0a0a;
    }
    .navbar-dropdown .navbar-item, .navbar-dropdown .navbar-link {
        color:black;
    }
    .navbar-link:not(.is-arrowless)::after {
        border-color: #fff;
    }
    .navbar-link:hover:not(.is-arrowless)::after {
        border-color: #e54b4b;
    }
    .navbar-start {
        margin: 0 auto;
        
    }
    .navbar-brand img {
        height: 16px;
    }
    .social {
        background: transparent;
        border-color: #fff;
        margin-left: 10px;
        color: white;
    }
    .social:hover {
        border-color: #e54b4b;
        color: #e54b4b;
    }
</style>