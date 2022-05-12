# Tech Details

add blah blah and subtending pages as we decide stuff

## OpenC2 Transfer Specifications

The mechanisms for exchanging OpenC2 Request (i.e., command) and
Response messages are defined in *transfer specifications*. The
[OpenC2
TC](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=openc2)
has published two transfer specifications as OASIS Committee
Specifications, documenting the use of HTTPS and
[MQTT](https://mqtt.org/) version 5.0. 

Here are links to the currently published specifications:

| | At OASIS | At GitHub
|---|:---:|:---:|
| MQTT | [HTML](https://docs.oasis-open.org/openc2/transf-mqtt/v1.0/transf-mqtt-v1.0.html) | [Markdown](https://github.com/oasis-tcs/openc2-transf-mqtt/blob/published/transf-mqtt-v1.0-cs01.md) |
| HTTPS | [HTML](https://docs.oasis-open.org/openc2/open-impl-https/v1.1/cs01/open-impl-https-v1.1-cs01.html) | [Markdown](https://github.com/oasis-tcs/openc2-impl-https/blob/published/open-impl-https-v1.1-cs01.md) |

Due to the complexities of establishing certificate-based mutual
authentication for HTTPS, MQTT is the preferred transfer protocol
for interoperability testing at the CAW. Participants should
become familiar with the transfer specification's requirements,
especially the topic structure. However, flexibility in the use
of topics is also potentially helpful during the plugfest (e.g.,
if there's a need to create separate communities using a single
message broker) so configurability is a desirable feature when
implementing MQTT for OpenC2.

### MQTT

MQTT is a message transfer protocol standardized under
[OASIS](https://www.oasis-open.org/). The MQTT Transfer
Specification uses [MQTT version
5.0](https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html),
as features added in that version of the protocol address OpenC2
needs. The HiveMQ website has [an excellent collection of
material](https://www.hivemq.com/mqtt-essentials/) about MQTT,
addressing both versions 3.1.1 and 5.0.

### Message Brokers

HII has established MQTT and OpenDXL message brokers on Google
Cloud Platform. Details for how to access those brokers will be
published here soon.

Connection process:
 - [OpenDXL Broker](OpenDxlBroker.md)
 - [MQTT Broker](MqttBroker.md)


## Return to Home
[return to Home](../index.md)
