```mermaid
                         +-------------------------+
                         |     User Interface      |
                         |  (Web / Chatbot / API)  |
                         +-----------+-------------+
                                     |
                                     v
                      +-------------------------------+
                      |  NLP Query Understanding Layer |
                      | (Intent Detection, Entity Extraction) |
                      +-------------------------------+
                                     |
                                     v
                     +----------------------------------+
                     |  Knowledge Graph Query Engine    |
                     | (Contextual + Semantic Matching) |
                     +------------------+---------------+
                                        |
       +----------------+---------------+----------------+-----------------+
       |                |                                |                 |
       v                v                                v                 v
+---------------+  +----------------+        +------------------+  +----------------+
| Static Content|  | Dynamic Web Data|        | Geospatial Data  |  | Metadata Index |
| (FAQs, Docs)  |  | (Live Feeds, APIs)|       | (Maps, Locations)|  | (Tags, Versions)|
+---------------+  +----------------+        +------------------+  +----------------+
        \                    |                          |                   /
         \___________________|__________________________|__________________/
                                        |
                                        v
                        +------------------------------+
                        |   Response Generator Layer    |
                        | (Summarization, Formatting)   |
                        +------------------------------+
                                        |
                                        v
                        +------------------------------+
                        |    Answer Delivered to User   |
                        +------------------------------+
```
