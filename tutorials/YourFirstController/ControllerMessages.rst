Sending & Receiving Messages
===================

.. code-block:: javascript

	connecter.on('SGUpdateMsg', function (data) {
		switch (data.MessageType) {
			case 'GameStarted':
				GameStarted(data.data);
				break;
			case 'MasterControl':
				MasterControl(data.data);
				break;
		}
	});
	connector.Send('MESSAGETYPE', data);