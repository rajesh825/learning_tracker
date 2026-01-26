
 ## Layer 1 Devices: Physical Layer

These devices deal with raw electrical or optical signals (bits).  They don't understand IP Addresses/Mac Addresses

### Hub

****How it Works:**** It takes an incoming signal on one port and blindly broadcasts it to all other ports

****Status:**** ****Obsolete.**** Replaced by Switches.

### Repeater

****How it Works:**** It receives a weak signal (due to attenuation over long cables), amplifies it, and retransmits it.

****Use Case:**** Extending WiFi range or Ethernet cables beyond 100 meters

### Modem (Modulator-Demodulator)

****Function:**** Connects your home network to the ISP (Internet Service Provider).
****How it Works:**** Converts digital signals from your computer into analog signals for telephone/cable lines (Modulation) and vice-versa (Demodulation).


## Layer 2 Devices: Data Link Layer

These devices work with ****MAC Addresses**** (Physical Addresses). 

### Switch

****Function:**** Connects devices in a LAN (Local Area Network).
****How it Works:**** Unlike a Hub, a Switch learns the MAC address of every connected device. It sends data ****only**** to the specific port where the destination device is connected.
****Benefit:**** Reduces collisions and improves security and speed.
 ****Types****
	****Unmanaged:**** Plug-and-play (Home/Small Office).
	*Managed:**** Configurable (VLANs, QoS) for enterprise use.

### Bridge

- ****Function:**** Connects two separate LAN segments to make them appear as one.
- ****How it Works:**** Filters traffic based on MAC addresses to keep local traffic local, reducing congestion. Largely replaced by Switches (which are essentially multi-port bridges).

### Access Point (AP)

- ****Function:**** Creates a Wireless Local Area Network (WLAN).
- ****How it Works:**** It acts as a bridge between wired Ethernet and wireless WiFi devices.

## Layer 3 Devices: Network Layer

These devices work with IP Addresses (Logical Addresses). They connect different networks together.

### Router

****Function:**** Connects multiple networks (e.g., your Home LAN to the Internet WAN).
****How it Works:**** It uses IP Addresses to determine the best path for data packets to travel. It maintains a Routing Table to make these decisions.
****Key Feature:**** Routers stop broadcast traffic, isolating networks from each other.

### Brouter (Bridging Router)

****Function:**** A hybrid device that acts as both a Bridge and a Router.
 ****How it Works:**** It can route known protocols (like TCP/IP) and bridge unknown protocols (like non-routable legacy traffic) at the same time. Rarely used today.

## Layer 4-7 Devices: Advanced Processing

### Gateway

- ****Function:**** A translator between two dissimilar networks.
- ****How it Works:**** It can convert protocols, data formats, or architectures (e.g., connecting a TCP/IP network to a legacy Mainframe network).
- ****Example:**** An "Internet Gateway" translates your private LAN requests into public internet requests.

### 10. Firewall

- ****Function:**** Security guard. Controls incoming and outgoing traffic based on security rules.
- ****Hardware:**** A physical appliance at the network edge.
- ****Software:**** Installed on a specific server/PC.
- ****Packet Filtering:**** Looks at headers (IP/Port).
- ****Stateful Inspection:**** Tracks active connections.


### Summary Table: Hub vs. Switch vs. Router

| ****Feature****      | ****Hub****        | ****Switch****           | ****Router****            |
| -------------------- | ------------------ | ------------------------ | ------------------------- |
| ****Layer****        | Layer 1 (Physical) | Layer 2 (Data Link)      | Layer 3 (Network)         |
| ****Address Type**** | None (Bits)        | MAC Address              | IP Address                |
| ****Data Flow****    | Broadcast (to all) | Unicast (to destination) | Route (best path)         |
| ****Intelligence**** | Dumb               | Smart                    | Smarter                   |
| ****Used For****     | Obsolete           | Connecting Devices (LAN) | Connecting Networks (WAN) |