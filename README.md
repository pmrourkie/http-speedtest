##What is this?
This is a simple Javascript that works out the throughput between a client, in this case your web browser and my server in Amsterdam.

##How does it work?
The throughput test works by taking the StartTime of when you start the test and then creates a binary file on the fly to download (You can test this yourself at http://speedtest.richardallen.co.uk/download?size=ENTERSIZE). The download request starts with a file size of 131072 bytes and doubles after each test, up to a maximum of 52428800 bytes. The EndTIme is then subtracted from the StartTime giving us the RunTime. In turn this allows us to work out the speed by dividing the FileSize by RunTime then by 1000 to give us the speed in Bytes Per Second. Before it is displayed on the screen it is translated into a more readable format by displaying it in either Bytes Per Second, Kilobytes per Second or Megabytes per second based on a certain threshold.

##Install/Run it yourself
You can grab the code from Github, of follow the below instructions:

1. Install the latest version of Node.js
2. Clone the git by opening terminal and typing: git clone https://github.com/rourkie/http-speedtest.git
3. In terminal, go to the http-speedtest directory
4. Run node ./bin/speed.js
5. Open up your browser and head to http://hostname:8080/ - This will be http://localhost:8080 if running locally.
You can change the port in /bin/config.js

##Issues
Lots, I imagine.

##Credits
This uses Knockout.js, JQuery-Ajax-Progress and an adapted version of Speedtest.