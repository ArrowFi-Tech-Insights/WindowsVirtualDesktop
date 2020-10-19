<h1>Host pools</h1>

<p>Host pool on kokoelma Azure virtuaali-koneista jotka toimivat Windows Virtual Desktop palvelussa session hosteina. Kaikkien samassa host poolissa sijaitsevien virtuaali-koneiden tulee pohjautua samaan käyttöjärjestelmä-imageen.</p>

<p>Host pooleja voi olla kahta tyyppiä.
<ul>
<li>Personal. Jokaiselle käyttäjälle dedikoidaan oma session host virtuaalikone jota käyttäjä käyttää jatkossa.</li>
<li>Pooled. Session hostit jaetaan useamman käyttäjän kesken.</li>
</ul>
</p>
<p>Tässä esimerkissä käytetään "pooled"-hostpoolia</p>

<p>Tällä hetkellä ainostaan Azuren US-regioonat ovat tuettuja Hostpoolien kanssa. Esimerkissä käytämme eastus regioonaa</p>
<p>Kun deployaat templatea muokkaa "Token Expiration Time" parametria niin että päivämäärä on tästä päivästa + 30 päivän sisään. Parametri määrittää hostpoolin rekisteröintiavaimen expiroitumispäivän.</p> 


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FArrowFi-Tech-Insights%2FWvdDemo%2Fmaster%2FHostPool%2Ftemplate.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/> </a>
