<h1>Arrow Tech Insights: Windows Virtual Desktop</h1>

<p>Tästä Github repositorystä löytyy toteutus Windows Virtual Desktop demoympäristölle.</p>
<p>Labrassa käytettävät Azure palvelut ja niiden hinnat:</p>
<ul>
<li>Azure Active Directory Domain Services (myöhemmin ADDS): https://azure.microsoft.com/en-us/pricing/details/active-directory-ds/</p>

<li>Windows Virtual Desktop (myöhemmin WVD): https://azure.microsoft.com/en-us/pricing/details/virtual-desktop/</li>
</ul>
<p>Suosittelemme poistamaan Azureen provisioidut palvelut heti labran jälkeen ylimääräisten kulujen välttämiseksi.</li>

<h2>Ympäristön pystyttäminen.</h2>

<p>1. Luo uusi resource group haluamallesi Azure regioonalle. Tässä esimerkissä käytämme resource grouppia nimeltä “wvd-demo” joka sijaitsee north europe regioonalla. Kyseistä resource grouppia käytetään ADDS ja WVD palveluille</p>
<p>2. Luodaan Active Directory Domain Services palvelu. Siirry ylemmästä tiedostolistausesta <a href="https://github.com/ArrowFi-Tech-Insights/WindowsVirtualDesktop/tree/master/ADDS">ADDS</a> kansioon ja etene ohjeen mukaan.</p>
<p>3. Luodaan HostPool Windows Virtual Desktop palvelulle. Siirry ylemmästä tiedostolistausesta <a href="https://github.com/ArrowFi-Tech-Insights/WindowsVirtualDesktop/tree/master/HostPool">HostPool</a> kansioon ja etene ohjeen mukaan.</p>
<p>4. Luodaan Virtuaalikoneet. Siirry ylemmästä tiedostolistausesta <a href="https://github.com/ArrowFi-Tech-Insights/WindowsVirtualDesktop/tree/master/VMs">VMs</a> kansioon ja etene ohjeen mukaan.</p>
<p>5. Luo uusi Azure AD käyttäjä ja liitä se se Application Groupin assigments osiosta</p>
