SGReconnect
=========

Node emits an 'SGReconnect' when a controller re-connects to the Fyo Node Server. The game should handle the player being re-added to the game at this point.

.. code-block:: javascript

	socket.on('SGReconnect', function(packet) {
		console.log(packet.PlayerId); // int
		console.log(packet.DeviceId); // string
	});
