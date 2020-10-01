<h1>Arrow Tech Insights: Windows Virtual Desktop</h1>

{% include youtubePlayer.html id="NQFtI3JLtaU&t" %}

<p>Tästä Github repositorystä löytyy toteutus Windows Virtual Desktop demoympäristölle.</p>
<p>Labrassa käytettävät Azure palvelut ja niiden hinnat.</p>

<p>Azure Active Directory Domain Services (myöhemmin ADDS): https://azure.microsoft.com/en-us/pricing/details/active-directory-ds/</p>

<p>Windows Virtual Desktop (myöhemmin WVD): https://azure.microsoft.com/en-us/pricing/details/virtual-desktop/</p>

<p>Suosittelemme poistamaan Azureen provisioidut palvelut heti labran jälkeen ylimääräisten kulujen välttämiseksi.</p>

<h2>Ympäristön pystyttäminen.</h2>

<p>1. Luo uusi resource group haluamallesi Azure regioonalle. Tässä esimerkissä käytämme resource grouppia nimeltä “wvd-demo” joka sijaitsee north europe regioonalla. Kyseistä resource grouppia käytetään ADDS ja WVD palveluille</p>
<p>2. Luodaan Active Directory Domain Services palvelu. Siirry ylemmästä tiedostolistausesta ADDS kansioon ja etene ohjeen mukaan.</p>
<p>3. Kun ADDS on luotu tulee ADDS palvelun mukana luotuun Vnet-verkkoon muuttaa DNS-palvelut niin että ADDS:n luoman domainin nimipalvelimet toimivat.</p>
<p>4. Luo domainjoiner@#valitsemasidomain#.onmicrosoft.com käyttäjä. Muista resetoida käyttäjän salasana luomisen jälkeen.</p>
<p>5. Luodaan HostPool Windows Virtual Desktop palvelulle. Siirry ylemmästä tiedostolistausesta HostPool kansioon ja etene ohjeen mukaan.</p>
<p>6. Luodaan Virtuaalikoneet. Siirry ylemmästä tiedostolistausesta VMs kansioon ja etene ohjeen mukaan.</p>
