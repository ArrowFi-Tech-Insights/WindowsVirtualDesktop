<h1>Arrow Tech Insights: Windows Virtual Desktop</h1>

{% include youtubePlayer.html id="n5Za_pHRbzI" %}

<p>Tästä Github repositorystä löytyy toteutus Windows Virtual Desktop demoympäristölle.</p>
<p>Labrassa käytettävät Azure palvelut ja niiden hinnat.</p>

<p>Azure Active Directory Domain Services (myöhemmin ADDS): https://azure.microsoft.com/en-us/pricing/details/active-directory-ds/</p>

<p>Windows Virtual Desktop (myöhemmin WVD): https://azure.microsoft.com/en-us/pricing/details/virtual-desktop/</p>

<p>Suosittelemme poistamaan Azureen provisioidut palvelut heti labran jälkeen ylimääräisten kulujen välttämiseksi.</p>

<h2>Ympäristön pystyttämisen vaiheet.</h2>

<p>1. Luodaan uusi resource group haluamallesi Azure regioonalle.</p>
<p>2. Luodaan ympäristölle Vnet, Active Directory Domain Services palvelu.</p>
<p>3. Luodaan HostPool sekä session host virtuaalikoneet Windows Virtual Desktop palvelulle.
<p>4. Luodaan testikäyttäjä sekä käyttäjäryhmä. Annetaan käyttöoikeus testikäyttäjälle</p>

<a href="https://github.com/ArrowFi-Tech-Insights/WindowsVirtualDesktop">Ohjeet löytyvät Arrow Tech Insights Github repositorystä</a>
