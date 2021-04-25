<script lang='ts'>
import Footer from "../Footer/Footer.svelte";
import Navbar from "../Navbar/Navbar.svelte";


class Rule {
    constructor(public section: String,public rules: String[]){}
}

let rules:Rule[] = [
    new Rule("Postanowienia ogólne",[
			"Gracz logując się na serwer akceptuje regulamin i oświadcza, że dołoży wszelkich starań by go przestrzegać.",
			"Podczas nałożenia blokady na konto gracza przedmioty związane z kontem mogą zostać usunięte.",
			"Nieznajomość regulaminu nie zwalnia gracza z odpowiedzialności za popełnione czyny",
			"Administracja ma prawo ukarać gracza za czyn nieuwzględniony w regulaminie który negatywnie wpływa lub może wpłynąć na serwer",
			"Oszustwa to znaczy oferowanie przedmiotu / usługi / pomocy a potem nie udzielanie tego przedmiotu / usługi / pomocy po uzgodnionej lub braku spełnienia danych warunków uzgodnionych przez obu graczy nie podlega zwrocie itemów osobie która została oszukana przez osobe która zaproponowała dany  przedmiot / usługe / pomoc",
			"Kopiowanie i używanie regulaminu serwera SpaceMC jest zabronione",
			"Regulamin może być zmieniony bez poinformowania graczy",
		]),
    new Rule ("Administracja ",[
			"Administrator nie ma zobowiązania podania powodu dlaczego gracz jest sprawdzany.",
			"Administracja ma prawo przejrzeć wszystkie pliki związane z Minecraft oraz te, które mogą zawierać potencjalne programy/modyfikacje ułatwiające rozgrywke [niedozwolone modyfikacje] bez zgody gracza.",
			"Administracja ma prawo poprosić gracza w każdej chwili o udostępnienie ss'ów oraz folderów/plików które mogą zawierać potencjalne programy/modyfikacje ułatwiające rozgrywke. Gracz jest zobowiązany do wykonania czynności.",
			"Administracja nieuczestnicząca w rozgrywce nie ingeruje w rozgrywkę na serwerze.",
			"Administracja nie sprzedaje i nie rozdaje przedmiotów. Uzyskanych na trybie kreatywnym",
			"Administracja nie odpowiada za szkody poniesione na koncie w skutek kradzieży konta.",
			"Administracja ma prawo wymagać od graczy zainstalowania programów: Discord (może być w wersji przeglądarkowej), TeamSpeak, TeamViewer, 7-zip, AnyDesk i Paladin w celu wykrycia niedozwolonych modyfikacji.",
            "Administrator może ukarać graczy w swój własny sposób(Kara nie będąca Mute/Ban/BanIP) dając graczowi karanemu wybór normalna kara lub kara administratora która zostanie poprzednio zgłoszona do zarządu z wyjaśnieniem plusów tego ukarania",
            "Administrator nie może nigdy używać kar z Art 2 §8 by mieć z tego korzyść na głównym świecie kara nie może być nigdy wykorzystywana do wzbogacania się administratora na głównym świecie"
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
            "Gracz dodaje oraz dołącza osoby do działki na własną odpowiedzialność.",
            "Zakaz bezsensownego griefowania terenu dookoła działki, jeśli celowo będziesz robił np. tzw. wulkany możesz zostać ukarany banem (zależne od szkód na terenie). ",
            "Zakaz kompletnego używania programu zmieniającego ip"
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
    ]),
    new Rule("Taryfikator",[
        "Obraza / Prowokacja / Spam na czacie - Mute od 10 minut do 7 dni",
        "Manipulacja pakietami odbiegającymi od Minecrafta (Od firmy Mojang) lub czytanie tych pakietów programami / urządzeniami (Chodzi tutaj o cheaty) - Ban od 7dni do 30 dni",
        "Brak kooperacji z administracją - Podwójna ilość czasu kary która mogła być wymierzona",
        "Wykorzystywanie błędów serwera w celu zdobycia przewagi - od 14 dni do Całkowita blokada konta(Perm)",
        "Inne rzeczy nie zawarte w taryfikatorze - Zależne od administratora",
        "Nadużycie rangi - Degrad"
    ]),
    new Rule("Zgłaszanie bugów",[
        "Bug jest to błąd serwerowy który został wprowadzony przez błąd ludzki oznacza to działanie mechanik serwera inne od przewidywanego",
        "Nagroda za zgłoszone bugi liczą się tylko jeśli są zgłoszone przez system zgłaszania issues na stronie github serwera https://github.com/SpaceMC-EU/SpaceMC-Bugi/issues",
        "Nagrody mogą być tylko przyznane jeśli zespół developerski uzna to za bug i zatwierdzi issue na githubie",
        "Nie nagradza się zgłaszania bugów na serwerze tylko przez system github",
        "Bugi dokładnie nie udokumentowane według wzoru zostaną pominięte i nie nagrodzone",
        "Każde 2 dni rangi niższej można wymienić na range premium wyższą do swagger\'a",
        "Brak informacji na temat nicku gracza skutkuje pominięciem przyznania nagrody po czasie naprawienia i zatwierdzenia",
        "Informacje na temat nicku gracza muszą być wydzielone od szablonu zgłaszania bugów najbardziej preferencyjnie na górze lub na dole szablonu oddzielone 2 enterami",
        "Rodzaj rangi i ilość dni może być zdefiniowana w poniższych punktach",
        "Bugi wizualne (Bugi które są tylko wyglądowe nie mechanikowe) - od 1h do 4 dni rangi Gold",
        "Bugi mechaniczne (Sprawiają że jedna opcja gry jest nie dostępna lub zepsuta bo nie da się użyć tej mechaniki według sposobu użycia) - od 1 dnia do 14 dni Rangi Gold",
        "Bugi dupe (Chodzi głównie o kopiowanie itemów i wykorzystywanie ich w grze później do zyskania przewagi) - od 30 dni rangi Gold\'a"

    ]),
    new Rule("Dodatki na serwer",[
        "Dodanie rzeczy na serwer może być tylko jeśli ilość głosów na tak będzie większa o 50% od totalnej ilości głosów na kanale propozycje serwera",
        "Werdykt każdej propozycji jest podejmowany po czasie 3dni roboczych od stworzenia propozycji",

    ])
];


</script>
<style lang="scss">
    #Rules {
        background: var(--background-main);
        height:100%;
        overflow: hidden auto;
    }
    h1, h2, a {
        margin: 0;
        font-family: 'Cinzel', serif;
        font-weight: normal;
        text-align:center;
        text-shadow: var(--glow);

    }
    h1 {
        .icon-logo{
            font-size:8vw;
        }
        font-size:10vw;
        color: #0a0;
        margin-top:10vh;
    }
    h2 {
        .icon-logo {
            font-size:4vw;
        }
        font-size:5vw;
    }
    .turnBack {
        background: #0b0;
        color: #fff;
        width:30%;
        padding: 1vw 3vw;
        font-size:2vw;
        border-radius: 3%;
        text-decoration:none;
        border: 1px solid var(--background-glow);
        display:block;
        margin: 3vh auto;
        transition: all .7s ease-in-out;
    }
    .turnBack:hover {
        color: var(--text-whiter);
        background: var(--text-camouflaged);
    }
    hr {
        width:99%;
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
    hr {
        color: var(--text-whiter);
        box-shadow: var(--glow);
    }
    .icon-logo {
        transform:rotate(-45deg);
    }

    img {
        border-radius: 100%;
        width:100%;
        display:block;
        margin-top:calc(98vh - 50px);
        margin-left:2vw;
        border:2px solid #0b0;
        transition: all .6s;
    }
    .image {
        position:absolute;
        width:50px;
    }
    .image:hover {
        img {
            width: 200px;
            margin-top:calc(98vh - 202px);
        }
    }
</style>
<Navbar/>
<section id='Rules'>
    <div class='image'>
        <img src='https://media.discordapp.net/attachments/770654936269848615/828617588371095562/grafikson-space.png' alt='spacemc'/>
    </div>
    <h1>Regulamin<br/><i class="fas fa-rocket icon-logo"></i>SpaceMC&trade</h1>
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
    <h2 style='color: #0a0;'><i class="fas fa-rocket icon-logo"></i>SpaceMC&trade</h2>
    <p style='color:#0a0; text-align:center; margin:0;'>
        Play with us!
    </p>
    <a class='turnBack' href='/'>Wróć na strone główną</a>
    <Footer/>
</section>

