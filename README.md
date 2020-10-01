<h1>Arrow Tech Insights: Windows Virtual Desktop</h1>
<p>Tästä Github repositorystä löytyy toteutus Windows Virtual Desktop demoympäristölle.</p>
<p>Labrassa käytettävät Azure palvelut ja niiden hinnat.</p>

<p>Azure Active Directory Domain Services (myöhemmin ADDS): https://azure.microsoft.com/en-us/pricing/details/active-directory-ds/</p>

<p>Windows Virtual Desktop (myöhemmin WVD): https://azure.microsoft.com/en-us/pricing/details/virtual-desktop/</p>

<p>Suosittelemme poistamaan Azureen provisioidut palvelut heti labran jälkeen ylimääräisten kulujen välttämiseksi.</p>

<h2>Ympäristön pystyttäminen.</h2>

<p>1. Luo uusi resource group haluamallesi Azure regioonalle. Tässä esimerkissä käytämme resource grouppia nimeltä “wvd-demo” joka sijaitsee north europe regioonalla. Kyseistä resource grouppia käytetään ADDS ja WVD palveluille</p>