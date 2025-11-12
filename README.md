# README
A repo containing all the public schemas related to conversation objects.

The file `conversation-public-components.yaml` represents the Conversation Entry Payload represents a single event or message in a conversation. Each payload follows the
ConversationEntry structure and contains an entry type that determines its specific schema.

The entryType field determines which schema to use for parsing the entryPayload.  The schema supports several types of entries, each extending from AbstractEntry.

For example,

* entryType:"Message" uses Message schema
* entryType:"ParticipantChanged" uses ParticipantChanged schema
* entryType:"RoutingResult" uses the RoutingResult schema


The schema uses discriminators to help identify specific types within abstract types. For example, in the Message schema, the AbstractMessage property can be a StaticContentMessage or FormResponseMessage or other message types.


