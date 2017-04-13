SGHandshakeIdentMsg
=========

Node emits an 'SGHandshakeMsg' when a controller connects to the Fyo Node Server. The game should handle the player being added to the game at this point.

.. code-block:: javascript

	socket.on('SGHandshakeIdentMsg', function(packet) {
		console.log(packet.PlayerId); // int
		console.log(packet.DeviceId); // string
	});
