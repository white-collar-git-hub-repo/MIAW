<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DDE0000044R3Q',
				'ghTestSite',
				'https://mcsg--dev.sandbox.my.site.com/ESWghTestSite1706538546589',
				{
					scrt2URL: 'https://mcsg--dev.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://mcsg--dev.sandbox.my.site.com/ESWghTestSite1706538546589/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

