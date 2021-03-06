This is a peer-to-peer concurrent rich text editing platform using Chord DHT(Distributed Hash Table).

Maintained 2 layer overlay network of chordal ring and k-ary tree to broadcast each message in O(logn) time. Extended Distributed Operational Transform algorithm to ensure the consistency of copies being concurrently updated in distributed nodes.

Important files:

1) main.py : Indexing server maintaining list of all open documents with just one IP which is required for new node to enter into the peer network handling a document.
2) Notepad.py : This file interacts with the front-end of application. Front-end is developed using pyQt4. Backend uses python socket programming.
3) Client.py : This file implements two layer overlay network of distributed hash table(DHT) using chordal ring and n-ary tree. It is responsible for communicating with other nodes.

Install pyqt4 before executing codes using:
sudo apt-get install python-qt4

Execution command:
indexing server: python main.py <IP> <PORT>
client application : python Notepad.py <PORT1> <PORT2> <ID> <ClientIP> <HostIP>
