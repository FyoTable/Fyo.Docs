AppHandshakeMsg
=========

An application emits an 'AppHandshakeMsg' with the node server.

.. code-block:: javascript

	socket.emit('AppHandshakeMsg', {
		AppIDString: 'string',
		BinaryData: 'base64 string',
		Controller: 'string'
	});


AppIDString
-------------

A unique string for your game. This key will store all of your unique controller files (optional).

BinaryData
-------------

If you have custom controllers for your game, you'll send a Base64 encoded Zip File containing all of your controller files.
The node server will then serve them via your AppIDString.

Ex: If your AppIDString is 'TicTacToe' then http://localhost:8080/TicTacToe will be the contents of your Zip File.

An index.html is the only required file in your Zip File.

Controller
-------------

The default controller to use. If Binary Data is provided, it points at a file contained with that Zip File.

If no Binary Data was provided it's used determine a controller other than the base_controller.