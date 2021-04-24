<script>
import { onMount } from "svelte";

import Body from "./Main/Body/Body.svelte";

function scrollFunc(){
    let content = document.getElementById('content');
	let squad = document.getElementById('Squad');
    
	let scroll = main.scrollTop;
	if(squad.offsetHeight/1.5 < scroll)
		return;
    scroll /= 2;
	content.style.backgroundPositionY = scroll+'px';
}
let main;
onMount( () => {
	main.addEventListener('scroll',scrollFunc,{passive: true});
	return () => {
		main.removeEventListener('scroll',scrollFunc,{passive:true});
	}
});

let rules = [
	{
		"Art 1. Postanowienia ogólne": [
			"1.Gracz logując się na serwer akceptuje regulamin i oświadcza, że dołoży wszelkich starań by go przestrzegać.",
			"2.Podczas nałożenia blokady na konto gracza przedmioty z kontem związane mogą zostać usunięte.",
			"3.Nieznajomość regulaminu nie zwalnia gracza z odpowiedzialności za popełnione czyny",
			"4.Administracja ma prawo ukarać gracza za czyn nieuwzględniony w regulaminie który negatywnie wpływa lub może wpłynąć na serwer",
			"5.Należy mieć na uwadze fakt, że niektórzy gracze mogą mieć złe intencje - mogą Ciebie zabić, oszukać, okraść itp. W takim przypadku musisz wiedzieć, że w obowiązach administracji nie leży karanie graczy z takimi intencjami.",
		]
	},
	{
		"Art 2. Administracja ":[
			"1.Administrator nie musi podawać powodu dlaczego gracz jest sprawdzany.",
			"2.Administracja ma prawo przejrzeć wszystkie pliki związane z Minecraft oraz te, które mogą zawierać potencjalne cheaty [niedozwolone modyfikacje] bez zgody gracza.",
			"3.Administracja ma prawo poprosić gracza w każdej chwili o udostępnienie ss'ów oraz folderów/plików które mogą zawierać potencjalne cheaty. Gracz jest zobowiązany do wykonania czynności.",
			"4.Administracja nieuczestnicząca w rozgrywce nie ingeruje w rozgrywkę na serwerze.",
			"5.Administracja nie sprzedaje i nie rozdaje przedmiotów.",
			"6.Administracja nie odpowiada za szkody poniesione na koncie w skutek kradzieży konta.",
			"7.Administracja ma prawo wymagać od graczy zainstalowania programów: Discord (może być w wersji przeglądarkowej), TeamSpeak, TeamViewer, 7-zip, AnyDesk i Paladin w celu wykrycia niedozwolonych modyfikacji.",
		]
	}
];



</script>
<style>
	main {
		height:100%;
		overflow-x: hidden;
	}
</style>
<svelte:head>
	<script src="https://kit.fontawesome.com/c0ff61a66a.js" crossorigin="anonymous"></script>
</svelte:head>
<main bind:this={main}>
	<Body/>
</main>
