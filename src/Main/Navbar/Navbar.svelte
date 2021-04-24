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
        ;
        li {
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
</style>
<nav>
    <i class="fas fa-rocket icon-logo"></i>
    <li>
        <ul><i class="fas fa-shopping-cart"></i> Sklep</ul>
        <ul><i class="fas fa-users"></i> Zespół</ul>
        <ul><i class="fas fa-file-alt"></i> Opis serwera</ul>
        <ul><i class="fas fa-vote-yea"></i> Zagłosuj</ul>
    </li>
</nav>