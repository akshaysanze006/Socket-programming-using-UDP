# Socket-programming-using-UDP

TCP guarantees the delivery of packets and preserves their order on destination. Sometimes  these features are not required and since they do not come without performance costs, it would be  better to use a lighter transport protocol. This kind of service is accomplished by the UDP protocol  which conveys datagram packet s. Datagram packets are used to implement a connectionless  packet delivery service supported by the UDP protocol. Each message is transferred from source  machine to destination based on information contained within that packet. That means, each packet  needs to have destination address and each packet might be routed differently, and might arrive in  any order. Packet delivery is not guaranteed.  
Java supports datagram communication through the following classes:  
• DatagramPacket  
• DatagramSocket  
 The class DatagramPacket contains several constructors that can be used for creating  packet object. One of them is: DatagramPacket(byte[] buf, int length, InetAddress address, int  port); This constructor is used for creating a datagram packet for sending packets of length length  to the specifi ed port number on the specifi ed host. The message to be transmitted is indicated in  the fi rst argument. The key methods of DatagramPacket class are: byte[] getData() Returns the  data buffer. int getLength() Returns the length of the data to be sent or the length of the data  received. void setData(byte[] buf) Sets the data buffer for this packet. void setLength(int length)  Sets the length for this packet. The class DatagramSocket supports various methods that can be  used for transmitting or receiving data a datagram over the network. The two key methods are:  void send(DatagramPacket p) Sends a datagram packet from this socket. void  receive(DatagramPacket p) Receives a datagram packet from this socket. A simple UDP server  program that waits for client’s requests and then accepts the message (datagram) and sends back  the same message is given below. Of course, an extended server program can manipulate client’s  messages/request and send a new message as a response. 


Algorithm 
• UDP Server: 
1. Start 
2. Create Datagram Socket
27 
Department of Computer Science and Engineering Vedavyasa Institute of Technology 
3. Now listen to a port 
4. Create empty byte array 
5. While (true) 
a. Create a Datagram Packet 
b. Receive Datagram Packet from client 
c. Now convert byte to string 
d. Print message 
 6. End While 
 7. Stop 
• UDP Client: 
 1. Start 
 2. Create Datagram Socket 
 3. While (true) 
 a. Get input from keyboard 
 b. Convert string to byte 
 c. Create a packet with destination, IP, port, address  d. Attach packet with byte array (data) 
 e. Send the packet 
 4. End While 
 5. Stop 
