AppHandshakeMsg
=========

An application emits an 'AppHandshakeMsg' with the node server to connect.

.. code-block:: javascript

	socket.emit('AppHandshakeMsg', {
		AppIDString: 'string',
		BinaryData: 'base64 string',
		Controller: 'string'
	});


AppIDString
-------------

A unique string for your game (no symbols or spaces, all lower-case). This key will tell node where to store your (optional) custom controllers.

BinaryData
-------------

If you have custom controllers for your game, you'll send a Base64 encoded Zip File containing all of your controller files.
The node server will then statically serve them via your AppIDString.

.. code-block:: javascript
	
	Example: If your AppIDString is 'TicTacToe' and you supply a Base64 Zip File with a file named Mark_X.png then you could access it with http://localhost:8080/TicTacToe/Mark_X.png where localhost is where the Fyo Node Server is running.

An index.html is the only required file in your Zip File.

Controller
-------------

The default controller to use. If Binary Data is provided, it points at a file contained with the Zip File provided.

If no Binary Data was provided the field is used to determine which controller is the default. ex: BaseController
