<button id="loadScriptButton">Load Chat Script</button>

<button onclick='embeddedservice_bootstrap.utilAPI.launchChat()'>Start Chat</button >


<script>
function loadExternalScript(scriptUrl) {
    // Check if the script is already loaded
    const existingScript = document.querySelector(`script[src="${scriptUrl}"]`);
    if (existingScript) {
        console.log('Script is already loaded, removing it.');
        existingScript.remove();
    }

    // Regardless of the existing script, load a new instance
    const script = document.createElement('script');
    script.src = scriptUrl;
    script.onload = function() {
        console.log('Script loaded successfully.');
    };
    script.onerror = function() {
        console.error('Error loading the script.');
    };
    document.body.appendChild(script);
}

document.getElementById('loadScriptButton').addEventListener('click', function() {
    loadExternalScript('https://mcsg--dev.sandbox.my.salesforce-sites.com/resource/McAfeeChatCode');
});
</script>
