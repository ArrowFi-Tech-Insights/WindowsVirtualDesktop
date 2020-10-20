<h2>Session Host Virtuaalikoneet</h2>

<p>Template provisioi seuraavat resurssit</p>
<ul>
<li>Session host virtuaalikoneet</li>
<li>Verkkointerfacet</li>
<li></li>
<li></li>
</ul>
<p>Session host-koneet liitetään luotuun Azure Active Directory Services domainiin ja session host-koneiden verkko-interfacet liitetään domainin network security grouppiin.</p> 

<p>Kun provisioit templaten, määritä parametrit admin username ja password sekä Hostpool Token. Hostpool Token löytyy Azure portaalista wvd-demo Host poolin alta "Overview" kohdasta "Registration key":n alta.</p>
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FArrowFi-Tech-Insights%2FWvdDemo%2Fmaster%2FVMs%2Ftemplate.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>