#### Scorecard API Instructions

*   **How to Invoke the Scorecard API which Returns JSON Data:**
    *   Endpoint
        *   POST: https://sitenv.org/scorecard/ccdascorecardservice2
    *   The POST method takes one parameter which is
        *   ccdaFile: The file that is being submitted for scoring
    *   Use the multipart/form-data to encode the file as part of the body parameters for the POST request

*   **How to Invoke the Scorecard API which Returns a PDF Report:**
    *   Endpoint
        *   POST: https://sitenv.org/scorecard/savescorecardservicebackend
    *   The POST method takes one parameter which is
        *   ccdaFile: The file that is being submitted for scoring
    *   Use the multipart/form-data to encode the file as part of the body parameters for the POST request. Note: The service _streams_ back the PDF data for consumption.

#### Scorecard External Tool Instructions

*   **How to Use the "One-Click" Scorecard Direct Email Service:**
      *   Using a HISP 
            1.   Send a Direct message with an attached C-CDA document (with an .xml extension) from your Direct email address to xxx@ds.sitenv.org (TODO: update to a publicly providable address or delete)
      *   Using your preferred email client (e.g. Mozilla Thunderbird)
            1.   Add a new email account with your Direct email address and settings
            2.   Send an email with an attached C-CDA document (with an .xml extension) from your Direct email address to xxx@ds.sitenv.org (TODO: update to a publicly providable address or delete)
                 * Troubleshooting Notes:
                     * Many (mainly consumer based, e.g. Comcast) ISPs block port 25. If this is the case for you, you will need to connect in another manner to use the service such as using a VPN or a mobile device hotspot.
      *   In either case, a detailed PDF report will be returned to the email address that sent the document to the "One-Click" Scorecard service. The report provides a rough quantitative assessment and highlights areas of improvement which can be made today to move the needle forward in interoperability of C-CDA documents.
    
    
*   **How to Use the Scorecard Batch Application:**
    *   Either download the instructions [here](https://github.com/siteadmin/scorecard-batch/raw/master/artifacts/Scorecard-%20Batch-%20Process-Instructions.docx) or read the following instructions:
        1.  Download the jar file from [https://github.com/siteadmin/scorecard-batch/tree/master/artifacts](https://github.com/siteadmin/scorecard-batch/tree/master/artifacts)

        2.  Please create the config file scorecard-batch.config with the following properties:

            *   scorecardBatch.ccdaFileLocation=/var/opt/scorecard/ccdaFiles

            *   scorecardBatch.outputFolderLocation=

            *   scorecardBatch.scorecardUrl=https://devccda.sitenv.org/scorecard/ccdascorecardservice2

            A sample config file can be found at [https://github.com/siteadmin/scorecard-batch/blob/master/src/main/resources/scorecard-batch.config](https://github.com/siteadmin/scorecard-batch/blob/master/src/main/resources/scorecard-batch.config)

            *   **scorecardBatch.ccdaFileLocation** - Folder location where all the CCDAs are placed for scoring. This is a mandatory property

            *   **scorecardBatch.outputFolderLocation** - Folder location to save the response files. If this is not specified a default folder scorecardBatchOutput is created in root folder and are saved to this location

            *   **scorecardBatch.scorecardUrl** - Specify the scorecard service end point for response. If this is not specified, the batch process will default to the Scorecard Production Server Endpoint

        1.  **Open Command Prompt and Run As Administrator**. Navigate to the location where the jar file is placed. For example, the jar file is placed under C:\Projects

            Execute the following command:
            
            ```bash
            java -DconfigFileLocation="C:/var/opt/scorecard/scorecard-batch.config" -jar scorecard-batch.jar
            ```

        1.  The response files will be created in the folder specified in the location specified in the **scorecardBatch.outputFolderLocation** property of the config file
