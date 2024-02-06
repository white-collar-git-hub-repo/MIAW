<script>
document.getElementById('initializeButton').addEventListener('click', function() {
    initEmbeddedMessaging(window.varLang);
});
</script>

<script>
    window.addEventListener("onEmbeddedMessagingReady", () => {            
        console.log( "Inside Prechat API!!" );
    embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( { "Queue_Name" : 'tesstt' } );
</script>

<script type='text/javascript'>
window.initEmbeddedMessaging =	function initEmbeddedMessaging(lang) {
		try {
			embeddedservice_bootstrap.settings.language = lang; // For example, enter 'en' or 'en-US'
			

			embeddedservice_bootstrap.init(
				'00DDE0000044R3Q',
				'McAfee_Chat',
				'https://mcsg--dev.sandbox.my.site.com/ESWMcAfeeChat1707158023631',
				{
					scrt2URL: 'https://mcsg--dev.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://mcsg--dev.sandbox.my.site.com/ESWMcAfeeChat1707158023631/assets/js/bootstrap.min.js'></script>

<button id="initializeButton">Initialize</button>

<button onclick='embeddedservice_bootstrap.utilAPI.showChatButton()'>Show button</button >

<button onclick='embeddedservice_bootstrap.utilAPI.launchChat()'>Launch Chat</button >
