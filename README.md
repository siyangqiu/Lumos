<h1>ReadMe</h1>
<h2>What is Lumos?</h2>
Lumos was a project built for ECS251 (Operating Systems) Winter Quarter 2020 at UC Davis as a part of a class project. It was inspired by <a href="https://arxiv.org/abs/1809.04774">Fidelius</a> and aimmed to achieve the same sort of protection (protecting secrets from a compromised host system/OS) while being more portable (Fidelius was built for a specific machine running a specific version of Ubuntu, GCC/G++, and Intel SGX) and easier to setup and use. Lumos is built from the ground up and makes different trade-offs in security vs usability. For more details check the PPT in this repo.

<h2>How is Lumos structured and how can I run it?</h2>

The Lumos Project is divided into 2 parts:
<ul>
<li>Server</li>
<li>Client</li>
</ul>

The Server components (in the server folder) are to be install on the Thin Client, while the Client components (in the client folder) are to be installed on the Host. (Terms thin client and host as described in the PPT). The server components are made up of a Chrome Extension and a Nodejs server for responding to requests made by the Chrome extensions. The client only has one component, another Chrome Extension.

To install the Chrome extensions:
<ol>
<li>Go to "about:extensions" in Chrome</li>
<li>Turn on Developer Mode (switch at the top right)</li>
<li>Click the "Load Unpacked" button and select the "Chrome Extension" folder for client or server respectively</li>
</ol>

Chrome extension configuration:<br>
On the host computer, right click on the Lumos icon and select "options". Enter the IP address of the Host computer. Make sure to use HTTP:// or HTTPS:// as configured in Lumos Server, as well as the correct PIN and ports.

Running Lumos Server:<br>
Navigate to lumos/server/Nodejs and follow the README.md file in that folder.

Additional 3rd Party software to be installed: <br>
Thin client:
<ul>
<li>Chrome</li>
<li>VNC Viewer</li>
</ul>
Host:
<ul>
<li>Chrome</li>
<li>VNC Server</li>
</ul>

Once all components have been installed, simply run Lumos Server on the thin client and VNC into the host computer.
