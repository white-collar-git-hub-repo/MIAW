<script>
    window.addEventListener("onEmbeddedMessagingReady", () => {            
        console.log( "Inside Prechat API!!" );
    embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( { "Queue_Name" : 'tesstt' } );
</script>

<script>
	function loadJws(){
		document.getElementById('loadBootstrapScript').addEventListener('click', function() {
		    // Check if the script is already loaded to prevent duplicates
		    if (!document.getElementById('dynamicBootstrapScript')) {
		        // Create a new script element
		        var scriptElement = document.createElement('script');
		        scriptElement.id = 'dynamicBootstrapScript'; // Assign an ID for potential future reference
		        scriptElement.type = 'text/javascript';
		        scriptElement.src = 'https://mcsg--dev.sandbox.my.site.com/ESWMcAfeeChat1707158023631/assets/js/bootstrap.min.js';
		        
		        // Define the onload handler
		        scriptElement.onload = function() {
		            initEmbeddedMessaging();
		        };
		
		        // Append the script element to the document's body
		        document.body.appendChild(scriptElement);
		    } else {
		        console.log('Bootstrap script is already loaded.');
		    }
		});
	}
</script>

<script id="dynamicScript" type="text/javascript">
       function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = window.varLang; // For example, enter 'en' or 'en-US'
			embeddedservice_bootstrap.settings.hideChatButtonOnLoad = true;

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

<button id="loadBootstrapScript" onclick="loadJws()">Load Script</button>

<button onclick="initEmbeddedMessaging()">Chat Online</button>

<button onclick='embeddedservice_bootstrap.utilAPI.launchChat()'>Start Chat</button >
