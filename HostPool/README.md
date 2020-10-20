<h2>Host pools</h2>

<p>Host pool on kokoelma Azure virtuaali-koneista jotka toimivat Windows Virtual Desktop palvelussa session hosteina. Kaikkien samassa host poolissa sijaitsevien virtuaali-koneiden tulee pohjautua samaan käyttöjärjestelmä-imageen.</p>

<p>Host pooleja voi olla kahta tyyppiä.
<ul>
<li>Personal. Jokaiselle käyttäjälle dedikoidaan oma session host virtuaalikone jota käyttäjä käyttää jatkossa.</li>
<li>Pooled. Session hostit jaetaan useamman käyttäjän kesken.</li>
</ul>
</p>
<p>Tässä esimerkissä käytetään "pooled"-hostpoolia</p>
<h1>Application Group</h1>
<p>Application group on looginen kokoelma session host virtuaalikoneille asennetuista sovelluksista. Application grouppeja on kahta eri tyyppiä<p>
<ul>
<li>Desktop. Käyttäjät saavat pääsyn työpöydälle.</li>
<li>RemoteApp. Käyttäjäy saavat pääsyn vain määritetylle sovellukselle.</li>
</ul>
<p>Application Groupeissa määritellään myös käyttäjien sovelluskohtaiset käyttöoikeidet<7p>

<h1>Workspace</h1>
<p>Workspace on looginen kokoelma application grouppeja. Jokaisen application groupin tulee olla liitettynä workspaceen jotta käyttäjät saa pääsyn sovelluksiin</p>

</p>

<p>Tällä hetkellä ainostaan Azuren US-regioonat ovat tuettuja Hostpoolien kanssa. Esimerkissä käytämme eastus regioonaa</p>
<p>Ennen kuin provisioint templaten, muokkaa "Token Expiration Time" parametria niin että päivämäärä on tästä päivästa + 30 päivän sisään. Parametri määrittää hostpoolin rekisteröintiavaimen expiroitumispäivän. Muut parametrit voit jättää oletus arvoille.</p>
<p>
Resurssit jotka template provisioi:
<ul>
<li>Hostpool (pooled)</li>
<li>Application Group </li>
<li>Workspace</li>
</ul>

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FArrowFi-Tech-Insights%2FWvdDemo%2Fmaster%2FHostPool%2Ftemplate.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/> </a>
