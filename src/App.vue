<template>
    <nav
        class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body"
    >
        <div class="container-fluid">
            <router-link class="navbar-brand" aria-current="page" to="/">
                Characters
            </router-link>
            <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarNav"
                aria-controls="navbarNav"
                aria-expanded="false"
                aria-label="Toggle navigation"
            >
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link
                            class="nav-link"
                            aria-current="page"
                            to="/"
                        >
                            Home
                        </router-link>
                        </li>
                        <li>
                        <router-link 
                            class="nav-link" 
                            aria-current="page" 
                            to="/about"
                        >
                            About
                        </router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <div class="main">
        <router-view></router-view>
    </div>
</template>