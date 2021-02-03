<script>
    import {Index} from "../index.js";
    import {getContext} from 'svelte';
    import DescriptionPopup from "./DescriptionPopup.svelte";
    import MatchPopup from "./MatchPopup.svelte";

    const {open} = getContext('simple-modal');

    let currIndex = 0;

    let fonds = [
        {
            "name": "Storebrand Fornybar Energi",
            "description": "Hei, takk for at du titter innom profilen min. Jeg er reiseglad, og foretrekker " +
                    "å oppleve verden fra sykkelsetet. Jeg liker å tenke nytt, og jeg elsker å diskut" +
                    "ere de store spørsmål over et godt glass brus. Ja, jeg drikker altså ikke alkoho" +
                    "l. Og du? Jeg ser heller ikke på porno. Vennene mine ser nok på meg som en event" +
                    "yrer med høy moral, en som ikke er redd for å ta sjanser, og som sier ifra hvis " +
                    "noe ikke er helt riktig. Hoppe fra en fjellskrent med paraglider? Ja, gjerne det" +
                    "! Delta i Skolestreik for klimaet? Absolutt!Er du som meg; liker å se verden med" +
                    " nye øyne, sykle gjennom vidstrakt natur og kanskje delta i en demonstrasjon mot" +
                    " krig? Ja, da synes jeg at du skal gi meg et hjerte!",
            "usp": [
                "Grønn", "Snill"
            ],
            "img": "./images/fornybar-energi.jpg",
            "link": "www.vg.no"
        }, {
            "name": "Storebrand Fremtid 10",
            "description": "Hei! Så hyggelig at du vil bli bedre kjent med meg!Jeg er en rolig person som ny" +
                    "ter livet best foran TV-en. Jeg er ganske glad i teknologi, og skaffer meg ofte " +
                    "det nyeste av det nye! Jeg klatrer ikke høyest og jeg løper ikke raskest, men sa" +
                    "tser i stedet på å nå målene mine over tid. Vennene mine vil beskrive meg som st" +
                    "ødig og litt nerdete. Ligner kanskje litt på Ludvig fra Flåklypa? Med sekken ful" +
                    "l av tekniske duppedingser. Ellers er jeg opptatt av å ta vare på naturen, at vi" +
                    " oppfører oss bra mot hverandre, og at vi tør å stå opp mot urettferdighet.Hvis " +
                    "du vil bli bedre kjent med meg, Lik da vel!",
            "usp": [
                "Livsnyter", "Varsom"
            ],
            "img": "./images/fremtid-10.jpg",
            "link": "www.vg.no"

        }, {
            "name": "Storebrand Fremtid 50",
            "description": "Halloisen! Jeg er en morsom skapning som liker ananas på pizza, ekstra sterk cur" +
                    "ry, og iskald brus i glasset. Jeg elsker å utforske naturen, enten til fots, ski" +
                    " eller sykkel. Besseggen har jeg ennå ikke gått, men kanskje klarer vi det samme" +
                    "n, hånd i hånd?Jeg ser på meg selv som en person med høy moralsk standard, og je" +
                    "g har innsett at skjønnhet er det første som falmer. For meg er det viktig at du" +
                    " tør å ta en sjanse, uten å bli dumdristig. Vil du gå ved min side og bli litt b" +
                    "edre kjent? You know what to do!  ",
            "usp": [
                "Naturbarn", "Nøisom"
            ],
            "img": "./images/fremtid-50.jpg",
            "link": "www.vg.no"

        }, {
            "name": "Storebrand Fremtid 100",
            "description": "Tjenare, nu kör vi! Jeg er en våghals med glimt i øyet, og jeg ser etter en som " +
                    "tør satse på meg. Du må være villig til å ta sjanser, og sammen skal vi finne ut" +
                    " at ofte nok er det verdt risikoen. Jeg elsker sterk mat, høylytte diskusjoner, " +
                    "fart, spenning, og alt som er gøy. Kroppen er mitt tempel, så den tar jeg godt v" +
                    "are på.Når folk først møter meg kan jeg virke spontan og vill, men egentlig er j" +
                    "eg veldig nøyaktig. Ja, jeg tar sjanser. Ja, jeg satser. Ja, jeg tør mer enn and" +
                    "re. Jeg er ikke farlig, det du ser er det du får!Er du med? Like da vel  ",
            "usp": [
                "Tøff", "Fremtidsrettet"
            ],
            "img": "./images/ofensivtoffing.jpg",
            "link": "www.vg.no"

        }, {
            "name": "Storebrand Norge Fossilfritt",
            "description": "Mitt livsmotto er Borte bra, men hjemme best. Jeg elsker norsk natur, så jeg tri" +
                    "ves best på ferie i eget land. Vi må ta vare på den vakre naturen vår. Jeg bor i" +
                    " Oslo, men er hverken hipster eller trendy. Kanskje litt mer sånn avslappet når " +
                    "det kommer til stil? Du må gjerne være moteriktig, men det er ikke det som betyr" +
                    " mest for meg.Vennene mine kaller meg rolig og nøktern. Jeg roper ikke høyest på" +
                    " fest, jeg drikker ikke alkohol, og jeg tar sterk avstand til gambling og porno." +
                    " Kanskje ikke noe man vanligvis skryter av allerede før første date, men det er " +
                    "viktig for meg at du vet det!Hvis du vil bli bedre kjent, Trykk hjerte!",
            "usp": [
                "Hjemmekjær", "Naturglad"
            ],
            "img": "./images/fosilfri.jpg",
            "link": "www.vg.no"

		},
		{
            "name": "Ingen flere fond i nærheten :(",
            "description": "Start på nytt eller sjekk ut Storebrand.no for flere fond!" ,
                    
                
            "usp": [
                "Storebrand", "valentinsdagen"
            ],
            "img": "./images/no-more.jpg",
            "link": "www.vg.no"

        }
    ];

    function renderNextFond() {
        let tmp = currIndex + 1;
        if (tmp == fonds.length) 
            return;
        
        currIndex++;
    }

    function likeFond() {
        open(MatchPopup, {
            name: fonds[currIndex].name,
			link: fonds[currIndex].link,
			image: fonds[currIndex].img
        });
    }

    function viewDescription() {
        open(DescriptionPopup, {
            name: fonds[currIndex].name,
            description: fonds[currIndex].description
        });
    }

    function refresh() {
        setTimeout(function () {
            location.reload()
        }, 100);
    }
</script>

<div class="flex-container container">

<div class="white-card">
    <Index
        descriptionCallback={viewDescription}
        image={fonds[currIndex].img}
        name={fonds[currIndex].name}
        description={fonds[currIndex].description}
        usp={fonds[currIndex].usp}/>
</div>
    <div class="row">
        <div class="yes-no-buttons">
            <div class="no-block">
                <button on:click={renderNextFond} onclick="this.blur();" class="but" id="nope">
                    <img src="images/X-04.svg" alt="X">
                </button>
            </div>
            <div class="yes-block">
                <button on:click={likeFond} onclick="this.blur();" class="but" id="yes">
                    <img src="images/Heart-green-01.svg" alt="heart">
                </button>
            </div>
        </div>
        <div class="reset-but">
            <button on:click={refresh} onclick="this.blur();" class="reset">
                <strong>Start på nytt</strong>
            </button>
        </div>
    </div>

</div>

<style>

	.white-card {
		background-color: #ffffff;
		padding-bottom: 2px;
		box-shadow: 0 1px 4px #c7c7c7;
		border-radius: 5px;

	}


	

    .but {
        height: 70px;
        width: 70px;
        border-radius: 100%;
        box-shadow: 0 1px 4px #c7c7c7;

    }

    .no-block,
    .yes-block {
        display: inline-block;
        float: left;
        width: 50%;
    }
    .no-block button {
        float: right;
        margin-right: 20px;
    }

    .yes-block button {
        margin-left: 20px;
    }

    .yes-no-buttons {
        width: 100%;
		position: relative;
		margin-top: 20px;
    }

    .reset-but {
		width: 100%;
        text-align: center;
    }
    .reset {
		padding: 10px 20px 10px 20px;
		margin-top: 20px;
		border-radius: 30px;
		box-shadow: 0px 0px 4px #da291c;
		min-width: 300px;

	}

	#yes img {
		width:40px;
		height: auto;
	}

	#nope img {
		width:40px;
		height: auto;
	}

</style>