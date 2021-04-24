<style lang="scss">
    #Squad {
        background: var(--background-main);
        border-top: 1px solid var(--text-whiter);
        border-bottom: 1px solid var(--text-whiter);
        box-shadow: 
        0 -1vh 3vh var(--text-whiter),
        0 20px 40px var(--background-glow);
        color: white;
        padding: 2vh 3vw;
    }
    h1,h2 {
        text-align:center;
        margin: 0;
    }
    .Team {
        display:flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-content: space-around;
    }
    .CharacterCard {
        width:20%;
        border-radius:.3vw;
        margin-top:10px;
    
        box-shadow: var(--glow);
        position: relative;
        overflow:hidden;
        img {
            z-index: -1;
            width: 100%;
            display:block;
        }
        h2 {
            font-size: 2vw;
            top: 0;
            left:0;
            margin-top: 75%;
            width:100%;
            height:100%;
            background: #191919;
            position:absolute;
        }
        .desc {
            font-size: 1.5vw;
            font-weight: 1;
        }
        background: rgb(11,11,11);
        background: linear-gradient(0deg, rgba(11,11,11,1) 71%, rgba(51,51,51,1) 100%); 
        padding: 2vh 2vw;
    }
    .Wlasciciel {
        color: #f00;
    }
    .Head-Admin {
        color: #f44;
    }
    .Moderator {
        color: #0a0;
    }
    .JuniorDev {
        color: #0b0;
    }
    .Trial-Support {
        color: #F70;
    }
</style>
<script lang='ts'>
    class Admin {
        public link: string;
        constructor(public nick:string,public rank:string){

        }
    }
    let link = 'https://photopass.appspot.com/3d.php?user=%%Nick%%&vr=0&hr=0&hrh=0&vrll=0&vrrl=0&vrla=0&vrra=0&displayHair=true&headOnly=false&format=png&ratio=20&aa=false&layers=true';
    
    let desc = [
        'Miły pomyślny chłopak pomagający w tworzeniu serwera zna się na promowaniu i zarządzaniu administracją',
        'Programista kontrolujący świat swojego komputera potrafiący zaginać czasoprzestrzeń by być bardziej leniwym',
        'Budownicza redaktorka i artysta z zamiłowaniem do budowania',
        'Programista nowy w zespole ale z chęciami',
        'сука блять',
        'Carola aka Karol jest naszym głównym działem pilnującym czat',
        'Ma tą jedną brew która wytwarza strach u cheaterów ale ogólnie spoko jest',
        'Anonimowy chłopak'

    ];
    
    let nicknames:Admin[] = [
        new Admin('ZmxDMG','Wlasciciel'),
        new Admin('LupusVirtute','Wlasciciel'),
        new Admin('Nnates','Head-Admin'),
        new Admin('Rekuseq','JuniorDev'),
        new Admin('Ruske','Moderator'),
        new Admin('Carola','Moderator'),
        new Admin('Zapiekanka_Heinz','Moderator'),
        new Admin('KenzX_PL','Trial-Support'),
    ];
    nicknames.forEach( (o)=> {
        let url = link;
        url = url.replace('%%Nick%%',o.nick);
        o.link = url;
    });
</script>
<section id='Squad'>
    <h1>Nasz zespół</h1>
    <br/>

    <div class='Team'>
        {#each nicknames as admin,i}
            <div class='CharacterCard'>
                <img src={admin.link} alt={admin.nick}/>

                <h2>
                    <p class={admin.rank}>
                      {admin.rank}
                    </p>
                    {admin.nick}
                    <br/>
                    <br/>
                    <div class='desc'>
                        {#if desc[i] != undefined}
                            {desc[i]}
                        {/if}
                    </div>
                </h2>
            </div>
        {/each}
    </div>
</section>