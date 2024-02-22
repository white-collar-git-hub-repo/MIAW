<script>
    const now = + new Date();
  const url = 'https://mcsg--dev.sandbox.my.site.com/resource/' + String(now) + '/McAfeeChatResources/css/McAfeeChatCSS.css';
  const link = document.createElement('link');
  link.setAttribute('href', url);
  link.setAttribute('rel', 'stylesheet');
  document.body.appendChild(link);
</script>

<button id="loadScriptButton">Load Chat Script</button>

<button onclick='embeddedservice_bootstrap.utilAPI.launchChat()'>Start Chat</button >


<script>
function loadExternalScript(scriptUrl) {
    // Check if the script has already been loaded
    if (!document.querySelector(`script[src="${scriptUrl}"]`)) {
        const script = document.createElement('script');
        script.src = scriptUrl;
        script.onload = function() {
            console.log('Script loaded successfully.');
        };
        script.onerror = function() {
            console.error('Error loading the script.');
        };
        document.body.appendChild(script);
    } else {
        console.log('Script is already loaded.');
    }
}

document.getElementById('loadScriptButton').addEventListener('click', function() {
    loadExternalScript('https://mcsg--dev.sandbox.my.salesforce-sites.com/resource/McAfeeChatCode');
});
</script>
