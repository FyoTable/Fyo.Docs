AppEndMsg
=========

Node emits an 'AppEndMsg' when the game should quit. This happens when there are no longer any controllers connected to the Fyo Node Server.

.. code-block:: javascript

	socket.on('AppEndMsg', function() {
		// Node told the game to end
	});
