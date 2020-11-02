<p>Tämä template luo Windows Virtual Desktop palvelun hallintaelementit ja session host virtuaalikoneet.</p>
<p>Windows Virtual Desktop palvelun hallintaelementit tukevat vain US regioonia tällä hetkellä joten esimerkissä sijoitamme ne eastus regioonalle. Session Host Virtuaalikoneet eivät ole sidottu US regioneihin ja ne sijoitetaan northeurope regioonalle.</p>
<p>Resurssit jotka template provisioi:</p>
<ul>
<li>Host pool (pooled)</li>
<li>Application Group </li>
<li>Workspace</li>
<li>Session Host virtuaalikoneet</li>
</ul>
<p>Oletus-parametrien mukaan template tekee pooled host poolin jossa session limit on 2 käyttäjä-sessiota per session host virtuaalikone</p>
<h2>Host pools</h2>

<p>Host pool on kokoelma Azure virtuaali-koneista jotka toimivat Windows Virtual Desktop palvelussa session hosteina. Kaikkien samassa host poolissa sijaitsevien virtuaali-koneiden tulee pohjautua samaan käyttöjärjestelmä-imageen.</p>

<p>Host pooleja voi olla kahta tyyppiä.
<ul>
<li>Personal. Jokaiselle käyttäjälle dedikoidaan oma session host virtuaalikone jota käyttäjä käyttää jatkossa.</li>
<li>Pooled. Session hostit jaetaan useamman käyttäjän kesken.</li>
</ul>
</p>
<p>Tässä esimerkissä käytetään "pooled"-host poolia sekä <a href="https://docs.microsoft.com/en-us/azure/virtual-desktop/host-pool-load-balancing">BreadthFirst</a> tyyppistä kuormantasausta</p>
<h2>Application Group</h2>
<p>Application group on looginen kokoelma session host virtuaalikoneille asennetuista sovelluksista. Application grouppeja on kahta eri tyyppiä<p>
<ul>
<li>Desktop. Käyttäjät saavat pääsyn työpöydälle.</li>
<li>RemoteApp. Käyttäjäy saavat pääsyn vain määritetylle sovellukselle.</li>
</ul>
<p>Application Groupeissa määritellään myös käyttäjien sovelluskohtaiset käyttöoikeidet</p>

<h2>Workspace</h2>
<p>Workspace on looginen kokoelma application grouppeja. Jokaisen application groupin tulee olla liitettynä workspaceen jotta käyttäjät saa pääsyn sovelluksiin</p>

<h2>Session Host virtuaalikoneet</h2>

<p>Session Host virtuaalikoneet tarjoavat käyttäjille työpöydän sekä koneille asennetut sovellukset.</p>
<p>

<h2>Templaten provisiointi</h2>

<p>1. Valitse Subscription ja Resource group.</p>
<p>Tällä hetkellä ainostaan Azuren US-regioonat ovat tuettuja Host poolien kanssa. Esimerkissä käytämme Host poolin osalta East US regioonaa. Muut resurssit provisioidaan North Europe regioonalle.</p>
<p>2. Määritä "Administrator Account Username" parametriin ADDS:n yhteydessä luoma domainjoiner@VALITSEMASIDOMAIN.onmicrosoft.com käyttäjänimi ja "Administrator Account Password
" kohtaan käyttäjän salasana.</p>
<p>3. Määritä "Vm Template" parametrin sisään valitsemasi domain.</p>
<p>4. Muokkaa "Token Expiration Time" parametria niin että päivämäärä on tästä päivästa + 30 päivän sisään. Parametri määrittää host poolin rekisteröintiavaimen expiroitumispäivän.</p>
<p>5. Määritä "Domain" parametriin valitsemasi domain.</p>
<p>Muut parametrit voit jättää oletusarvoille.</p>

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FArrowFi-Tech-Insights%2FWvdDemo%2Fmaster%2FHostpool_and_vms%2Ftemplate.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/> </a>

<h2>Templaten provisioinnin jälkeen</h2>
<p>1. Luo AzureAD ryhmä. Käyttäjäryhmän jäsenet pääsevät käyttämään juuri luotua WVD ympäristöä. </a></p>
<p>2. Luo testikäyttäjä ja lisää se juuri luomaasi ryhmään.
<p>3. Liitä luomasi AzureAD ryhmä luomaasi Application Grouppiin. Search "Application groups" -> Valitse luomasi Application groups -> Valitse "Assigments" -> valitse +Add ja lisää luomasi AzureAD ryhmä.</p>
<p>4. Kirjaudu Windows Virtual Desktop palvelun Workspaceen oheisen <a href="https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-windows-7-10">ohjeen</a> mukaisesti 