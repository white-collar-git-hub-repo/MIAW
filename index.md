<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.hideChatButtonOnLoad = true;
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DDE0000044R3Q',
				'MIAW_Chat_Without_PreChat_QueueBased',
				'https://mcsg--dev.sandbox.my.site.com/ESWMIAWChatWithoutPreC1705495884793',
				{
					scrt2URL: 'https://mcsg--dev.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://mcsg--dev.sandbox.my.site.com/ESWMIAWChatWithoutPreC1705495884793/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
