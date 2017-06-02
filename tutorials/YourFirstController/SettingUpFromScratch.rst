Setting up a Controller from Scratch
===================

The controller has a connection to the Fyo Server via Socket.io (WebSockets). Socket.io is served up via the Fyo Server, which means socket.io has to be included via

.. code-block:: html

	<script src="/socket.io/socket.io.js"></script>

The next javascript library to be included is the Fyo Game Table API, which is also served up via the Fyo Server and is included via

.. code-block:: html

	<script src="/fyogametable/dist/fyo.js"></script>

Now that the two required libraries are loaded, we just need to start the connection.

.. code-block:: javascript

	var connector = new FYO.FyoConnection('APPID');

Next up is adding controls, and interacting with the connector