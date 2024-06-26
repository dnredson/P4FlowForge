## TrafficForge

Traffic Forge introduces novel capabilities that are particularly beneficial to P4 programmable networks. 

While Traffic Forge offers integration with P4 programmable networks, it is essential to emphasize that its utility is not limited to environments with P4 switches. This versatile tool is designed to support standard protocols, including TCP, UDP, HTTP, and MQTT, making it an asset for many network testing scenarios beyond P4-specific applications. Whether it is evaluating the performance of a conventional network, testing the resilience of network applications against varied traffic patterns, or validating the behavior of network protocols under different conditions, Traffic Forge stands out for its adaptability. This universal applicability ensures that Traffic Forge is not just a tool for cutting-edge P4 network environments but a comprehensive solution for network testing and performance evaluation across various infrastructures and protocols.

Documentation: https://dnredsons-organization.gitbook.io/traffic-forge/

Docker Image: dnredson/trafficforge

#Using this tool

#TCP

	generator.py --time <time> --mean <messages_per_second> --interface <output_interface> --port <port> --protocol tcp --target <target_ip>

	receiver.py --protocol tcp --port <port>

#UDP 

	generator.py --time <time> --mean <messages_per_second> --interface <output_interface> --port <port> --protocol udp --target <target_ip>

	receiver.py --protocol udp --port <port>
	
#HTML 

	generator.py --time <time> --mean <messages_per_second> --interface <output_interface> --port <port> --protocol html --header "<header>" --target <target_ip>

	receiver.py --protocol html --port <port>
	
#MQTT 

	generator.py --time <time> --mean <messages_per_second> --interface <output_interface> --protocol mqtt --topic <topic> --target <broker_address>

	receiver.py --protocol mqtt --source <broker_address> --topic <topic>
	
#Custom Protocol

  	generator.py --time <time> --mean <messages_per_second> --interface <output_interface> --protocol custom --custom <json_file>

  	receiver.py --protocol custom --custom <json_file>
