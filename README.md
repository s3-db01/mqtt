# MQTT
## Installation
Install the docker container on your system. This can be done via `docker pull mtolmtomt/mqtt-client`. After you install this
you can run the project via CMD using `docker run -p 2020:2020 mtolmtomt/mqtt-client`. This needs to
be done because otherwise the ports of the websocket aren't connected right. You can **NOT** run it in
docker desktop with the start button.
## Reasoning
We chose a websocket for the communication to the backend. This is because there will need to be
a constant update if we get a new message.  If we use a websocket for this it will be able to update
the message when there is a new message recieved. When we use a API the backend will need to constantly
check the API link if something has changed. In this case we can let them connect to the websocket and they 
can run a function when the websocket sends new information about the sensors.
