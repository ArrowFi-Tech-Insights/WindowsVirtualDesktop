<h1>Host pools</h1>

<p>Host pool on kokoelma Azure virtuaali-koneista jotka toimivat Windows Virtual Desktop palvelussa session hosteina. Kaikkien samassa host poolissa sijaitsevien virtuaali-koneiden tulee pohjautua samaan käyttöjärjestelmä-imageen.</p>

<p>Host pooleja voi olla kahta tyyppiä.
<ul>
<li>Personal. Jokaiselle käyttäjälle dedikoidaan oma session host</li>
<li>Pooled. Session hostit jaetaan useamman käyttäjän kesken.</li>
</ul>
</p>


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FArrowFi-Tech-Insights%2FWvdDemo%2Fmaster%2FHostPool%2Ftemplate.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>