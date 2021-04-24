<script>
import Footer from "../Footer/Footer.svelte";
import Navbar from "../Navbar/Navbar.svelte";
import Squad from "../Squad/Squad.svelte";
import Description from "../Description/Description.svelte";
import { onMount } from "svelte";
import { mainSection } from '../../App.svelte';

    let image = './images/background.png';
    function scrollFunc(){
        let content = document.getElementById('content');
        let squad = document.getElementById('Squad');
        
        let scroll = mainSection.scrollTop;
        if(squad.offsetHeight/1.5 < scroll)
            return;
        scroll /= 2;
        content.style.backgroundPositionY = scroll+'px';
    }

onMount( () => {
	mainSection.addEventListener('scroll',scrollFunc,{passive: true});
	return () => {
		mainSection.removeEventListener('scroll',scrollFunc,{passive:true});
	}
});
</script>
<style lang="scss">
    @import "./Body.scss";
    #content {
        width:100%;
        height:100%;
    }
</style>
<!-- 
<div id="background" style='background: no-repeat url({image})'>
</div> -->


<Navbar/>
<div id="content" style='background: no-repeat url({image}); background-size: cover;'>
    <div class="logo">
        <i class="fas fa-rocket"></i>
        SpaceMC.EU
    </div>
</div>
<Squad/>
<Description/>
<Footer/>