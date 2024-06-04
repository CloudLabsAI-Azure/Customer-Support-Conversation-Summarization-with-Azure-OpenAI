# Customer Support Conversation Summarization with Azure OpenAI

## Lab Overview

Most businesses provide customer service support to help customers with product queries, troubleshooting, and maintaining or upgrading features or the product itself. To provide a satisfactory resolution, customer support specialists need to respond quickly with accurate information. OpenAI can help organizations with customer support in a variety of ways. 

In this hands-on lab, you’ll learn how to generate summaries of customer-agent interactions in various customer support scenarios by using the Azure OpenAI model. The focus of this lab is to provide efficient and accurate summarization of conversations, improving the quality of customer support. 

## Architechture Diagram

![Architechture Diagram](media/architechture-diagram.png)

## Understanding Azure's AI Language Service 

Azure AI Language Service is a managed cloud service that simplifies the development of natural language processing (NLP) applications. With minimal machine-learning expertise required, it allows users to: 

- **Identify Key Terms and Phrases:** Quickly extract significant words and expressions from text.
  
- **Analyze Sentiment:** Determine the emotional tone behind words to understand the context better.
  
- **Summarize Text:** Condense long documents into shorter, digestible summaries using both extractive and abstractive techniques.
   
- **Build Conversational Interfaces:** Create intelligent chatbots and virtual assistants that can engage with users naturally. 

## Key Features

- **Extractive summarization:** Produces a summary by extracting salient sentences within the document.

- **Multiple extracted sentences:** These sentences collectively convey the main idea of the document. They're original sentences extracted from the input document's content. 

- **Rank score:** The rank score indicates how relevant a sentence is to a document's main topic. Document summarization ranks extracted sentences, and you can determine whether they're returned in the order they appear, or according to their rank. 

- **Multiple returned sentences:** Determine the maximum number of sentences to be returned. For example, if you request a three-sentence summary extractive summarization returns the three highest scored sentences.

- **Abstractive summarization:** Generates a summary that doesn't use the same words as in the document but captures the main idea.

- **Summary texts:** Abstractive summarization returns a summary for each contextual input range within the document. A long document can be segmented so multiple groups of summary texts can be returned with their contextual input range. 

- **Contextual input range:** The range within the input document used to generate the summary text. 

## Lab Overview

In this Hands-on-lab, you will perform the following tasks.

- Provision Azure AI Language Service
- Summarize the customer-agent conversation in Azure AI Language Studio
