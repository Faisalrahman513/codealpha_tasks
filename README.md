# codealpha_tasks
def packet_callback(packet):
    if packet.haslayer("IP"):  # Check if packet contains IP layer
        print(f"Source: {packet['IP'].src} --> Destination: {packet['IP'].dst} | Protocol: {packet.proto}")

sniff(prn=packet_callback, store=False)
