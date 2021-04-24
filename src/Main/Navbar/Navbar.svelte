<style lang="scss">
    nav {
        display:flex;
        flex-direction: row;
        justify-content: space-between;
        align-items:center;
        padding:.5vw 2vw;
        position: absolute;
        z-index: 1;
        width:calc(100vw - 4vw);
        color: #fff;
        .icon-logo {
            transform: rotate(-45deg);
            font-size: 1.5em;
            margin-top: .5vh;
        }
        background-color: rgba($color: #000000, $alpha: .2);
    }
    nav {
        box-shadow: 0px 1px 10px #0B0;
        color: var(--text-whiter);
        text-shadow: var(--glow);
        font-size: 1.2vw;
        li {
            ul {
                transition: all .7s ease-in-out;

            }
            display:flex;
            :hover {
                color: var(--text-selected);
                cursor: pointer;
                
            }
        }
    }
    li {
        list-style-type: none;
    }
    a {
        color:inherit;
        text-decoration: none;
    }
</style>
<script>
import { onMount } from 'svelte';
import { scrollto } from "svelte-scrollto";
import * as animateScroll from "svelte-scrollto";
animateScroll.setGlobalOptions({
    container: 'main'
});
</script>
<nav>
    <i class="fas fa-rocket icon-logo"></i>
    <li>
        <ul><a href="#/"><i class="fas fa-clipboard"></i> Strona Główna</a></ul>
        <ul><a href="#/Rules"><i class="fas fa-clipboard"></i> Regulamin</a></ul>
        <ul><a href='#/' use:scrollto={'#Squad'}><i class="fas fa-users"></i> Zespół</a></ul>
        <ul><a use:scrollto={'#Description'} href='#/'><i class="fas fa-file-alt"></i> Opis serwera</a></ul>
        <ul><a href='https://lista-serwerow.emecz.pl/serwery/minecraft/707cb592-5290-4f48-930e-9061efc945c1'><i class="fas fa-vote-yea"></i> Zagłosuj</a></ul>
        <ul><i class="fas fa-shopping-cart"></i> Sklep</ul>
    </li>
</nav>