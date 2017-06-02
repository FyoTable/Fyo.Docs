Thumbsticks & Buttons
===================

Built in renderables

* FYO.ThumbStick2D
* FYO.ThumbStick3D
* FYO.DPad2D
* FYO.DPad3D
* FYO.Button2D
* FYO.Button3D

.. code-block:: javascript

    var thumbstickLeft = new FYO.ThumbStick3D(connecter, {
        container: 'mainContainer', // Which element ID to place it in (optional, will default to body)
        onmoved: function (data) { // When an update happens
			// This will automatically do a connector.Send event internally on the connector
			// using a the generic 20 number array system
            connecter.SetAxis(FYO.AXIS[0], data.x, FYO.AXIS[1], -data.y);
        }
    });           
	
.. code-block:: javascript

	var buttonRenderer = new FYO.Button2D(connecter, {
		container: 'mainContainer', // Which element ID to place it in (optional, will default to body)
		image: '/fyogametable/assets/imgs/Button_B_2D.png', // image used to render the button, this is built in
		ondown: function () {
			// This will automatically do a connector.Send event internally on the connector
			// using a the generic 20 number array system
			connecter.SetButtonOn(FYO.BUTTON[0]);
		},
		onup: function () {
			// This will automatically do a connector.Send event internally on the connector
			// using a the generic 20 number array system
			connecter.SetButtonOff(FYO.BUTTON[0]);
		}
	});