# ipfs
IPFS - InterPlanetaryFileSystem is a long needed upgrade to the conventional HTTP protocol.
While HTTP is Client-Server based, IPFS is decentralized and uses bit like tech for file sharing.
The future of internet is here, what are we waiting for. Let's begin

Step 1 - Download the repository
Step 2 - For Linux/MacOS : tar xvfz go-ipfs.tar.gz
         mv go-ipfs/ipfs /usr/local/bin/ipfs
Step 3 - ipfs help 

After this you have ipfs installed on your system 

Step 4 - ipfs init
initializing ipfs node at /Users/jbenet/.go-ipfs
generating 2048-bit RSA keypair...done
peer identity: Qmcpo2iLBikrdf1d6QU6vXuNb6P7hwrbNPW9kLAH8eG67z
to get started, enter:

  ipfs cat /ipfs/QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG/readme

Step 5 -  Note the hash there may differ. If it does, use the one you got.

Now, try running:

ipfs cat /ipfs/QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG/readme
You should see something like this:

Hello and Welcome to IPFS!

██╗██████╗ ███████╗███████╗
██║██╔══██╗██╔════╝██╔════╝
██║██████╔╝█████╗  ███████╗
██║██╔═══╝ ██╔══╝  ╚════██║
██║██║     ██║     ███████║
╚═╝╚═╝     ╚═╝     ╚══════╝

If you're seeing this, you have successfully installed
IPFS and are now interfacing with the ipfs merkledag!


You can explore other objects in there. In particular, check out quick-start:

Step 6 - ipfs cat /ipfs/QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG/quick-start

Which will walk you through several interesting examples.
Going Online

Once you’re ready to take things online, run the daemon in another terminal:

Step 7 - ipfs daemon
Initializing daemon...
API server listening on /ip4/127.0.0.1/tcp/5001
Gateway server listening on /ip4/127.0.0.1/tcp/8080

Wait for all three lines to appear.
Make note of the tcp ports you get. if they are different, use yours in the commands below.

Now, if you’re connected to the network, you should be able to see the ipfs addresses of your peers:

Step 8 - ipfs swarm peers
/ip4/104.131.131.82/tcp/4001/ipfs/QmaCpDMGvV2BGHeYERUEnRQAwe3N8SzbUtfsmvsqQLuvuJ
/ip4/104.236.151.122/tcp/4001/ipfs/QmSoLju6m7xTh3DuokvT3886QRYqxAzb1kShaanJgW36yx
/ip4/134.121.64.93/tcp/1035/ipfs/QmWHyrPWQnsz1wxHR219ooJDYTvxJPyZuDUPSDpdsAovN5
/ip4/178.62.8.190/tcp/4002/ipfs/QmdXzZ25cyzSF99csCQmmPZ1NTbWTe8qtKFaZKpZQPdTFB

These are a combination of <transport address>/ipfs/<hash-of-public-key>.

Now, you should be able to get objects from the network. Try:

ipfs cat /ipfs/QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ/cat.jpg >cat.jpg
open cat.jpg

And, you should be able to give the network objects. Try adding one, and then viewing it in your favorite browser. In this example, we are using curl as our browser, but you can open the IPFS URL in other browsers as well:


They also have a web console you can use to check the state of your node. On your favorite web browser, go to:

    http://localhost:5001/webui

How friggin cool is this?

References - ipfs.io
