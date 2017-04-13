SGDisconnectMsg
=========

Node emits an 'SGDisconnectMsg' when a controller disconnects from the Fyo Node Server. The game should handle the player no longer being in game at this point.

.. code-block:: javascript

	socket.on('SGDisconnectMsg', function(packet) {
    console.log(packet.PlayerId); // int
    console.log(packet.DeviceId); // string
	});
