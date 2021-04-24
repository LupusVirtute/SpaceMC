<script lang='ts'>
class Rule {
    constructor(public section: String,public rules: String[]){}
}

let rules:Rule[] = [
    new Rule("Postanowienia ogólne",[
			"Gracz logując się na serwer akceptuje regulamin i oświadcza, że dołoży wszelkich starań by go przestrzegać.",
			"Podczas nałożenia blokady na konto gracza przedmioty z kontem związane mogą zostać usunięte.",
			"Nieznajomość regulaminu nie zwalnia gracza z odpowiedzialności za popełnione czyny",
			"Administracja ma prawo ukarać gracza za czyn nieuwzględniony w regulaminie który negatywnie wpływa lub może wpłynąć na serwer",
			"Oszustwa to znaczy oferowanie przedmiotu / usługi / pomocy a potem nie udzielanie tego przedmiotu / usługi / pomocy po uzgodnionej lub braku spełnienia danych warunków uzgodnionych przez obu graczy nie podlega karaniu osoby która zaproponowała dany  przedmiot / usługe / pomoc",
		]),
    new Rule ("Administracja ",[
			"Administrator nie ma zobowiązania podania powodu dlaczego gracz jest sprawdzany.",
			"Administracja ma prawo przejrzeć wszystkie pliki związane z Minecraft oraz te, które mogą zawierać potencjalne programy/modyfikacje ułatwiające rozgrywke [niedozwolone modyfikacje] bez zgody gracza.",
			"Administracja ma prawo poprosić gracza w każdej chwili o udostępnienie ss'ów oraz folderów/plików które mogą zawierać potencjalne programy/modyfikacje ułatwiające rozgrywke. Gracz jest zobowiązany do wykonania czynności.",
			"Administracja nieuczestnicząca w rozgrywce nie ingeruje w rozgrywkę na serwerze.",
			"Administracja nie sprzedaje i nie rozdaje przedmiotów. Uzyskanych na trybie kreatywnym",
			"Administracja nie odpowiada za szkody poniesione na koncie w skutek kradzieży konta.",
			"Administracja ma prawo wymagać od graczy zainstalowania programów: Discord (może być w wersji przeglądarkowej), TeamSpeak, TeamViewer, 7-zip, AnyDesk i Paladin w celu wykrycia niedozwolonych modyfikacji.",
        ]
    ),
    new Rule("Gracze",[
            "Zakazane jest używanie Zhackowanych klientów gry (np. Huzuni, Nodus, Resilience, itp.) - ban 30 dni.",
            "Dozwolone modyfikacje: ReisMinimap oraz Optifine + Shadery. (To znaczy modyfikacje które nie dają informacji dających przewagę nad graczami typu XRay / Wallhack itp. itd.).",
            "Używanie wersji Minecrafta które ułatwiają rozgrywke poprzez modyfikowanie plików gry / pamięci gry / manipulują pakietami wysyłanymi do serwera np. : Wurst Huzuni Nodus Jigsaw jest nie dozwolone",
            "Używanie resource packów które są uznawane jako xray to znaczy gracz może wizualnie w grze widzieć przez bloki innych graczy surowce itp jest zabronione",
            "Używanie błędów serwera bez poinformowania administratora jest karane zależnie od administratora takie błędy należy niezwłocznie zgłaszać na githubie https://github.com/SpaceMC-EU/SpaceMC-Bugi/issues",
            "Brak kooperacji z administracją serwera jest karane",
            "Jest zakaz tworzenia multikont bez powodu typu (zmiana nicku,skradzione konto premium itp itd) jest karane to banem permanetnym na adres ip na całą edycje serwera",
            "Zakaz udostępniania konta innym osobom takie konta są banowane.",
            "Używanie obraźliwych i wulgarnych pseudonimów na serwerze grozi banem permanetnym na ten konkretny pseudonim. (chyba że adres ip użył tego psuedonimu przez co grozi mu ban na ip)",
            "Współpraca z cheaterem grozi blokadą konta, wyczyszczeniem ekwipunku i usunięciem działki, każdy cheater powinien być niezwłocznie zgłoszony administracji serwera.",
            "Gdy jest się podejrzanym o złamanie regulaminu przenoszenie ekwipunku do innych graczy / miejsc skutkuje czyszczeniem ekwipunku i działki tego gracza",
            "Wylogowanie się podczas sprawdzania skutkuje banem zależnym od podejrzeń administratora.",
            "Przyznanie się do niedozwolonych modyfikacji podczas sprawdzania skraca bana do tygodnia.",
            "Zakaz szerzenia błędnych / nieprawdziwych informacji na temat serwera.",
            "Zakaz wzbogacania sie kosztem serwera, zakaz sprzedawania kont, przedmiotów w grze za realną walutę.",
            "Oszukiwanie i/lub wprowadzanie administracji w błąd może skutkować banem permanentnym(Zależne od administratora).",
            "Gracz ma obowiązek mieć włączony czat, w przeciwnym wypadku może zostać zbanowany z powodu braku odzewu podczas sprawdzania w celu wykrycia niedozwolonych modyfikacji.",
            "Gracz dodaje oraz dołącza do działki na własną odpowiedzialność.",
            "Zakaz bezsensownego griefowania terenu dookoła działki, jeśli celowo będziesz robił np. tzw. wulkany możesz zostać ukarany banem (zależne od szkód na terenie). ", 
    ]),
    new Rule('Czat', [
        "Obraza graczy / administracji / serwera / rodziny graczy lub administracji grozi mutem lub banem.",
        "Spamowanie / floodowanie na chacie / helpopie grozi mutem lub banem.",
        "Reklamowanie innych serwerów / stron internetowych / filmów / treści pornograficznych grozi mutem lub banem.",
        "Udostępnianie danych osobowych i prywatnych (nazwiska, numery telefonów, zdjęcia, Facebooki itp.) grozi mutem lub banem.",
        "Zakaz ogłaszania ofert niezwiązanych z grą Minecraft na czacie globalnym.",
        "Zakaz przekręcania nicków administracji i szydzenia z niej.",
        "Udostępnianie adresów IP graczy grozi banem.",
        "Jakiekolwiek groźby skierowane w kierunku graczy/administracji mogą być karane banem. ",
    ])
];


</script>
<style lang="scss">
    #Rules {
        background: var(--background-main);
        height:100%;
        overflow:auto;
    }
    h1,h2 {
        margin: 0;
        font-family: 'Cinzel', serif;
        font-weight: normal;
        text-align:center;
    }
    h1 {
        font-size:10vw;
        color: #0a0;
        text-shadow: var(--glow);
    }
    h2 {
        font-size:5vw;
        text-shadow: var(--glow);

    }
    p {
        text-align: center;
        font-size: 1.5vw;
    }
    .Rule {
        color: #FFF;
        .RuleColor {
            color: #0b0;
            font-weight: 900;
        }
    }
</style>
<section id='Rules'>
    <h1>Regulamin SpaceMC</h1>
    {#each rules as rule,i}
        <h2>Art {i+1}. {rule.section}</h2>
        <section class='Rules'>
            {#each rule.rules as individual,j}
            <p class='Rule'>
                <span class='RuleColor'>§{j+1}.</span> {individual}
            </p>
            {/each}
        </section>
        <hr/>
    {/each}
</section>