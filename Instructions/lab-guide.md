# Hands-On Lab - Customer Support Conversation Summarization with Azure OpenAI

## Task 01 - Provision Azure AI Language service

1. In the Azure portal, search for **Azure AI services (1)** and select **Azure AI Services (2)** from the services list.

   ![](../media/azure-ai.png)

2. On the **Azure AI Services** blade, select **Language Sevice (1)** and click on **Create (2)**.

   ![](../media/azure-ai-language.png)

3. On the **Select additional features** blade, under **Custom features** settings, select **Custom text classification, Custom named entity recognition, Custom summarization, Custom sentiment analysis & Custom Text Analytics for health** and click on **Continue to create your resource**.

   ![](../media/azure-ai-language-create00.png)
  
4. On the **Create Language** blade, under the **Basics** tab, enter the following details, click on **Review + create** and then **Create**.

   - Subscription: **Select your Default Subscription (1)**
   - Resource group: **Select your Default Resource group (2)**
   - Region: **Select your Default Region (3)**
   - Name: **language-service-<inject key="Deployment-ID" enableCopy="false"/> (4)**
   - Pricing tier: **S (1 k Calls per minute) (5)**
   - New/Existing storage account: **New storage account (6)**
   - Storage account name: **openaistorage<inject key="Deployment-ID" enableCopy="false"/> (7)**
   - Storage account type: **Standard LRS (8)**
   - **Check the box for the Responsible AI Notice (9)**

   ![](../media/azure-ai-language-create-01.png)

   ![](../media/azure-ai-language-create-02.png)
   
6. Wait for the deployment to succeed. Once the deployment is succeeded, click on **Go to resource group**.

   ![](../media/go-to-rg-01.png)

     <validation step="f85ecad5-8ad9-4288-8696-abbae27b058e" />

     >**Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
     > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
     > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
     > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.


## Task 02 - Summarize the customer-agent conversation in Azure AI Language Studio

1. In the Azure portal, on the resource group blade, navigate to the **language-service-<inject key="Deployment-ID" enableCopy="false"/>** Language service.

   ![](../media/navigate-language-service.png)

2. On the Language service Overview pane, under **Get Started**, select **Get started with Language Studio**.

   ![](../media/language-get-started.png)

3. The Language Studio opens up in a new tab, in the **Select an Azure resource**, for the Resource name dropdown, select your language service and click on **Done**.

   >**Note:** Sign in to Language Studio using your Azure credentials from the **Environmnet** tab if not signed-in already.
    
   >**Note:** Leave the Azure diectory, Azure subscription and Resource type as default.

   ![](../media/language-studio-select00.png)

   - If you don't get the Select an Azure Resource pop-up, then click on **Select a resource** in your Language Studio.

   ![](../media/language-studio-select01.png)
   
5. In your Azure AI Language Studio, in the **Featured** tab, select **Try it now** for the **Summarize information**.

   ![](../media/language-summarize-info.png)

6. On the **Summarize information** blade, under the **Documents** tab, select your preferred language, azure resource that you deployed, number of sentences you prefer in summary and specify your summary interest.

   ![](../media/language-summarize-info01.png)

7. In the text box, copy and paste the below conversation between a customer and an agent. The conversation is about a customer having trouble accessing their account, verifying their identity, troubleshooting, and successfully resolving the issue.

   >**Note:** Select **Both** for Summary Types to get both the Extractive and Abstractive summarization.

   ```
   Agent: Hi there! Thank you for contacting us today. How can I assist you?

   Customer: Hi! I'm having trouble accessing my account. I keep getting an error message whenever I try to log in.

   Agent: I'm sorry to hear that. Let's see what we can do to get you back into your account. Could you please provide me with your account username or email address?

   Customer: Sure, it's john.doe@example.com.

   Agent: Great, thank you for that. Just to confirm, could you also provide the last four digits of the credit card associated with your account? It's just a security measure.

   Customer: Of course, it's 1234.

   Agent: Perfect, thank you for verifying. Let me take a look at your account now... Hmm, it seems like there might be a temporary issue on our end. Have you tried accessing your account from a different device or browser?

   Customer: No, I haven't. But I can give it a try.

   Agent: That would be helpful. Sometimes these issues are browser or device-specific. Let me know if you're able to log in from a different device or browser.

   (Customer tries accessing the account from another device.)

   Customer: It worked! I was able to log in from my phone.

   Agent: That's great to hear! It seems like the issue might be related to your original device or browser settings. If you encounter any further problems, feel free to reach out to us again. Is there anything else I can assist you with today?

   Customer: No, that's all for now. Thank you so much for your help!

   Agent: You're very welcome! If you have any other questions or concerns in the future, don't hesitate to contact us. Have a wonderful day!
   ```

   ![](../media/language-text-box.png)

8. Check the box to acknowledge and click on **Run**.

   ![](../media/language-acknowledge.png)

9. Once the model runs successfully, you will get both the extractive and abstractive summaries for the customer-agent conversarion on the **Result** tab based on the selected number of sentences in summary.

   ![](../media/conversation-result.png)

10. Review the **Rank Score** of the sentences under Original text.

    ![](../media/orginal-text-rank-score.png)

11. You can also review the extractive and abstractive results in JSON foramt on the **JSON** tab.

    ![](../media/json-tab.png)

## Task 03 - Provision Azure AI Speech service

1. In the Azure portal, search for **Azure AI** and select **Azure AI Services** from the services list.

   ![](../media/azure-ai.png)

2. On the **Azure AI Services** blade, select **Speech Sevice (1)** and click on **Create (2)**.

   ![](../media/speech-service.png)
  
3. On the **Create Speech Services** blade, under the **Basics** tab, enter the following details, click on **Review + create** and then **Create**.

   - Subscription: **Select your Default Subscription (1)**
   - Resource group: **Select your Default Resource Group (2)**
   - Region: **Select your Default Region (3)**
   - Name: **speech-service-<inject key="Deployment-ID" enableCopy="false"/> (4)**
   - Pricing tier: **Standard S0 (5)**
  
   ![](../media/speech-service-create-01.png)

6. Wait for the deployment to succeed. Once the deployment is succeeded, click on **Go to resource**.

   ![](../media/speech-go-to-resource.png)

     <validation step="fdc5b686-2e7b-43db-ba7a-f69384575b3e" />

     >**Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
     > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
     > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
     > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.


## Task 04 - Analyze sentences and call summary of audio recordings in Azure AI Speech Studio

1. In the Azure portal, on the resource group blade, navigate to the **speech-service-<inject key="Deployment-ID" enableCopy="false"/>** Speech service.

   ![](../media/navigate-speech-service.png)

2. On the Speech service Overview pane, under **Get Started**, select **Go to Speech Studio**.

   ![](../media/speech-service-did.png)

3. The Speech Studio opens up in a new tab, under **Speech capabilities by scenario**, click on **Try out post call transcription** for the **Post call transcription and analytics**.

   ![](../media/speech-studio-select.png)

4. The Post call transcription and analytics gives an overview of the **Call center transcription and analytics with Azure Speech and Language** and it's common use cases along with a few sample audio recordings of the customer-agent conversation where you can analyze the sentences and the call summary.

5. In the **Try it out > Try with Samples** tab, click on the **Play** button for listen to the sample audio conversation between the customer and the agent.

   ![](../media/speech-studio-try-samples.png)

6. In the **Analyze sentences** tab, analyze the Sentiment and the Transcript between Speaker1 and Speaker2.

   ![](../media/analyze-sentences.png)

7. Turn Off the **Hide PII** toggle to view the Speakers' Personal Identifiable Information (PII).

   >**Note:** The **Hide PII** toggle is tuned On by default.

8. Once you have analyzed the sentences between the two speakers, click on the **Call summary** to view the **Issue summary** and the **Resolution summary** fo the conversation.

   ![](../media/call-summary.png)

9. Now, let's try uploading custom audio recordings to analyze and fetch the call summary. In the **Try it out > Upload your own data** tab and configure the following details:

    - Resource for Speech service: **speech-service-<inject key="Deployment-ID" enableCopy="false"/> (1)**
    - Resource for Language service: **language-service-<inject key="Deployment-ID" enableCopy="false"/> (2)**
    - Acknowledge the checkbox **(3)**
    - Click on **Browse files... (4)** to upload the custom audio files
  
    ![](../media/upload-own-data.png)

10. Navigate to **C:\LabFiles\Recordings** folder and upload the audio recordings individually and wait for the upload to complete.

    ![](../media/audio-files.png)

11. Click on the **Play** button to listen to the audio file, analyze the sentences **(1)** and the call summary **(2)** of the uploaded audio recordings.

    ![](../media/upload-analyze-sentences.png)

    ![](../media/upload-call-summary.png)

## Review

In this hands-on lab, you have accomplished the following:

- Provisioned Azure AI Language service
- Summarized the customer-agent conversation in Azure AI Language Studio
- Provisioned Azure AI Speech service
- Analyzed sentences and call summary of audio recordings in Azure AI Speech Studio










   
