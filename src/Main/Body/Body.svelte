<script lang='ts'>
import Footer from "../Footer/Footer.svelte";
import Navbar from "../Navbar/Navbar.svelte";
import Squad from "../Squad/Squad.svelte";
import Description from "../Description/Description.svelte";

    let image = './images/background.png';
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