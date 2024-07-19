# Text_To_Chart_using_LLM
LLMs have shown their ability to transform unstructured text into a Knowledge Graph. However, the majority of examples I have seen allow the LLM to decide what ontology/schema to use. Some have added restrictions on what properties to use. I want to create graphs that conform to a specific ontology/schema for the following reasons:

I will want to create a variety of different queries over the resulting graph. Creating queries without knowledge of the schema is close to impossible.
I will want to create graphs from a large number of documents, so large that they cannot be processed as a single prompt despite the increasing size of allowable prompts. I will want all graph responses to conform to the same ontology.
In the past NLP tools were available to extract a graph from unstructured text, but these tools were not easily accessible for casual use.

Previously I demonstrated that this can be done by prompting an LLM with the ontology, but this is token-expensive.

Using LLM to transform unstructured text to KG
I want to describe and compare four approaches that use an LLM to transform unstructured text, responding with a KG that conforms to a pre-defined ontology:

1.Text-to-Graph using an LLM with pre-trained ontologies<\br>
2.Text-to-Graph prompted an LLM with an ontology
3.Text-to-Graph using an LLM fine-tuned with an ontology
4.Text-to-Graph using a hybrid of a fine-tuned and pre-trained LLM
