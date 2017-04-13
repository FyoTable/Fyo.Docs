SGUpdateMsg
=========

Node emits an 'SGUpdateMsg' when a controller sends an update. The packet data can contain anything you set your custom controller to send. You determine how to handle/process the data with the MessageType field.

.. code-block:: javascript

	socket.on('SGUpdateMsg', function(packet) {
		console.log(packet.PlayerId); // int
		console.log(packet.DeviceId); // string
    console.log(packet.MessageType); // string
    console.log(packet.data); // json object
    switch(packet.MessageType) {
      case 'Points':
        alert('You gained ' + packet.data + ' points!');
        break;
    }
	});
