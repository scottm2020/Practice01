
# Getting Started with AEM 6.5

## Table of Contents

* [Lab Overview](#lab-overview)
Need to update table of Contents


## Lab Overview

New to Experience Manager? This introductory session highlights its support for fluid experiences. Highlights: • Introduction to e-commerce in Experience Manager • Assets integration with Adobe Stock and custom tagging • Using workflows for fluid experiences...

### Key Takeaways

* Identify usecases to choose between Experience Fragmenst & Content Fragments. 
* Introduction to E-Commerce in AEM 
* Adobe Stock Integration Integration and custom tagging

### Prerequisites

* AEM 6.5 L22
* Configuration of AEM with Adobe Stock
* Configuration of Smart Tagging
* E-Commerce namespace loaded into Adobe IO

## Lesson 1 - Using Content Fragments in AEM

### Objective

1. Determine usage of content fragments
2. Create content fragment models.
3. Create content fragments using content fragment model
4. Add variations in content fragments.
5. Download Content Fragments
6. Use editing capabilities of content fragments
7. Expose JSON from Content Fragments

### Lesson Context

In this lesson , we will learn how to use content fragments in AEM, and explore their benefitss. We will create content fragments using an underlying schema conten defined in the content fragment model. We will also explore variations and a few other features of content fragments.

#### Exercise 1.1

In this exercise we will create an initial **Content Fragment Model** .

1. Go to AEM > Tools > Assets > Content Fragment Models
  
   ![Figure 1: Content Fragment Models ](./images/cfmodel.jpeg)
  
2. Double click to open the We.Retail folder.

3. Press the **Create** button to create a model

    ![Figure 1: Content Fragment Models Create Button ](./images/createbtn.jpeg)


4. Provide model details
   
    * Model Title : Article
    * Description : Content Fragment Model for Articles in We.Retail (optional)

5. Press **Create** Button and you should get a success message.

     ![Figure 1: Content Fragment Models Create Button ](./images/cfmodelsuccess.jpeg)

6. Press **Open** button in success message.

#### Exercise 1.2

In this exercise we will add fields to the Article Content Fragment Model.

1. On your screen you should see **Content Fragment Model Editor** . It is divided into two sections, the left-one is canvas where will add fields and on the right side we have Data Type lists which shows us list of all data types which can be added to content fragments.
    
  ![Figure 1: Content Fragment Models Editor ](./images/cfmeditor.jpeg)

2. Click on **Single line text** data type and drag it on canvas to add it. 

3. Go to **Properties** tab and add following details
   * Field Label :Article Title
   * Property Name : articleTitle  (required field)
   * Placeholder : Enter Article Title
   * Required : Checked

![Figure 1: Single Line Text ](./images/cfmsingle.jpeg)

4. Select **Data Types** to return to the field selection area. Add another **Single line text** to the canvas with the following properties
   * Field Label :Article Author
   * Property Name : articleAuthor  (required field)
   * Placeholder : Enter Article Author Name
   * Required : Unchecked

5. Add **Multi line text** to the canvas  with following properties
   * Field Label :Article Body
   * Property Name : articleBody  (required field)

![Figure 1: Completed Content Fragment Model ](./images/cfmcomplete.jpeg)

6. Press **Save** button to compelete creation of Article Content Fragment Model.


#### Exercise 1.3

Now that we have a content fragment model, we will use it to create a content fragment.

1. Go to AEM > Assets > Files > We.Retail > English
2. Create a folder by pressing **Create** btton and provide title as **CF**.
3. Open **CF** folder
4. Press Create Button > Content Fragment . You should see a list of available content fragments.
   
   ![Figure 1: Content Fragment Model List ](./images/cfmlist.jpeg)

5. Click on **Article** template or content fragment model and Press **Next** button.

6. Provide title for the content fragment as **North Slope Adventures**.
   
7. Press Create Button and you should get Success Message. Press **Open** button in success message modal-window.

Now you should see a form with all data types we provided in article content fragment model. In this exercise we will be adding content to the content fragment Model


8.  Add following content to this article.
    * Article Title  : North Slope Adventure
    * Article Author : Your Name or Any name
    * Article Body   :  [Text from file](images/cftext1.txt) 

  ![Figure 1: Content Fragment ](./images/cf1.jpeg)

9. Press **Save** button to save this article

#### Exercise 1.4 

As content owner , we also want to create content fragment variations for other channels and requirements.

1. Select recently created content fragment
2. Select Edit or Press **E** on your keyboard to Edit Content Fragment.
3. Press **Create Variation** to create new variation of the content fragment.
4. Provide Title as **Summary** and Press **Add**

![Figure 1: Summary Variation  ](./images/cfsummaryv.jpeg)

> We will be using OOTB summarization feature for content fragments to summarize the article. 
1. Click in Article Body box and select maximize icon
![Figure 1: Maximize ](./images/cfmax.jpeg)

2. In maximize window, Press **Summarize Text** Button
![Figure 1: Maximize ](./images/cfwords.jpeg)

3. Provide Target words as **200**
4. Review the summarized results and Press **Summarize** Button to confirm final Summarization.
5. Select the text area and press **minimize** icon.
6. Press **Save** button to save summary.


#### Exercise 1.5 Downloading Content Fragments


1. Navigate to the content fragements in AEM Assets
2. Click **Download** to download the content fragments and choose elements
![Figure 1: Maximize ](./images/cfdownload.jpeg)

3. Open the zip file and examine the content

#### Exercise 1.6 Editoral Capabilities and using in web pages of Content Fragments

1. Click into a content fragment and choose a multi line text field.
2. Select the annotate field in order to set up collaboration with other authors
![Figure 1: Maximize ](./images/cfannotate.jpeg)

3. Add a annotation

4. Open a content fragment and choose timeline to compare.
![Figure 1: Maximize ](./images/cfversion.jpeg)

#### Exercise 1.7 Exporting content fragments as JSON

1. Create a new page template from the weRetail empty page template with the name API Page
2. Use WeRetail content policy and be sure content fragements can be aded. Be sure to enable the template
3. Create a page from that templatem and create an API page for organization and then an article page
4. Add some content fragments to the page. Configure the elements you want added to the page
5. Make a request to the resource with model.json in the URL as shown.

![Figure 1: Maximize ](./images/cfexpose.jpeg)

## Lesson 2 - Using Experience Fragments in AEM

### Objective

1. Determine usage of Experience Fragments.
2. Differentiate between Experience Fragments & Content Fragments.


### Lesson Context

Experience Fragments allows content authors to reuse content across channels including sites pages and 3rd party systems.



#### Exercise 1.1


1. Go to AEM Navigation > Experience Fragments.
2. Create two language folders with following titles
   * en
   * de
  
3. Select **en** folder and Press Create > Experience Fragments. This will list OOTB templates for Experience Fragment Creation.

    > Experience Fragment templates are like Page Templates.

4. Select ** We.Retail Experience Fragment Web Variation** template.
5. Press **Next** button and provide **Title** of experience fragment as **Adventure in North Slope**
6. Press **Create** button and Press **Open** in success message.
   
   > You should see a Experience Fragment Page Editor, it is quite similar to AEM Page Editor.
7. Add following components to the Layout Container :
   
   *  **Title Component**
   *  **Image Component**
   *  **Content Fragment Component**
   
8.  Resize Image Component and Content fragment to get them in same row.
   
 ![Figure 1: Experience Fragment](./images/xf2.jpeg)

9. Now add an image to image component
10. In Asset browser , filter the list by Content Fragment
    
    ![Figure 1: Experience Fragement ](./images/xfcf.jpeg)

11. Now drag the content fragment on content fragment Component on Page.
12. Double click to open dialog box of content fragment.
13. Configure Content Fragment Dialog box 
    * Display Mode : Single Text Element
    * Element : Article Body

  ![Figure 1: Content Fragment Models ](./images/xfsingle.jpeg)

14. In Paragraph Tab, Select Range **Radio Button** and provide input as **2-3**. This determines to show only second to third paragraph.

  ![Figure 1: Content Fragment Models ](./images/xf-para.jpeg)

15. Press check or done button to save changes.

  ![Figure 1: Content Fragment Models ](./images/xfpreview.jpeg)

  #### Exercise 1.2

  1. Setup Target cloud configuration in Cloud Services
  2. Configure cloud configuration on folder
  
  ![Figure 1: Cloud Services     ](./images/efCloudService.jpeg)

  3. Open the Experience Fragment you created and publish it to Target by clicking **Export to Target** and **Publish**

  ![Figure 1: Publish Services     ](./images/efPublishtoTarget.jpeg)

  4. Open in Adobe Target and note the HTML and JSON version of the experience fragment.

  ![Figure 1: Export to Target     ](./images/efExport.jpeg)

  6. Return to AEM and use the **Delete from Target Button** to delete the offer from Adobe Target. 

   ![Figure 1: Delete from Target     ](./images/efdelete.jpeg)


## Lesson 3 - Understanding how E-Commerce works with AEM

### Objective

1. Explore how AEM Makes E-Commerce calls through OpenWhisk
2. Explore how Adobe I/O works with E-Commerce


### Lesson Context

AEM uses the E-Commerce framework with Adobe IO to make instanteous calls to the back end e-commerce system without having to store the information in AEM. In this exercise, you will explore how e-commerce and Adobe I/O work together.

![Figure 1: Overview](images/ecommerceoverview.jpeg)


#### Exercise 1.1

In this exercise, you will use a simple client to send parameters to Adobe I/O just as it would send or recieve e-commerce information such as price, inventory etc. 

1. Open a terminal window on your machine.


![Figure 1: Overview](images/terminalwindow.jpeg)

  
2. **cd** into the L764 folder

3. Checkout the e-commerce code from the Adobe Central GitHub repository using the following command.

   ```js
  git clone https://github.com/Adobe-Marketing-Cloud/adobe-cif-extension-sample.git 

   ```

4. **cd** into the adobe-cif-extension-sample/exercise-01 folder

5. Create an OpenWhisk package making sure to use a format seat-firstname-lastname

 ```js
wsk package create seat-YOUR_FIRSTNAME-YOUR_LASTNAME
 ```
6. Create an action for hello world using the sample provided.

```js
wsk action create seat-YOUR_FIRSTNAME-YOUR_LASTNAME/hello-world hello-world.js
 ```

 7. Execute and see the results with parameters:
```js
wsk action invoke seat-YOUR_FIRSTNAME-YOUR_LASTNAME/hello-world --result --param firstName Gary --param lastName Kirsten

 ```
8. Invoke the action using the param-file flag and passing the parameters.json file.

```js
wsk action invoke seat-{YOUR_FIRSTNAME}-{YOUR_LASTNAME}/hello-world --result --param-file parameters.json

 ```
## Lesson 4 - Integrate AEM Assets with Adobe Stock

### Objective

1. Search and Preview AEM Stock Assets directly from AEM 
2. License and save assets directly to the AEM Digital Assets Manager

### Lesson Context

AEM 6.5 provides users the ability to search, preview, save and license Adobe Stock assets directly from AEM. Organizations can now integrate their Adobe Stock Enterprise plan with AEM Assets to make sure that licensed assets are now broadly available for their creative and marketing projects, with the powerful asset management capabilities of AEM. 

#### Exercise 1.1

1. From the main screen of AEM, choose **Assets** and select **Search Adobe Stock**.

2. Search for **hiking** in Adobe Stock and select an unlicensed asset.

3. Examine the options in the toolbar and then select **View Similiar from Adobe Stock**

![Figure 1: Overview](images/ashiking.jpeg)

4. Select an image and choose **View in Adobe Stock**

5. Examine the image and explore the options available in Adobe Stock. 

6. Navigate back to AEM and save the asset by selecting **save** and choose the folder you wish to save it in. 

![Figure 1: Overview](images/asaveimage.jpeg)

#### Exercise 1.2

In this exercise, you will use Smart Tagging to automatically tag images

1. Use AEM's Omnisearch to search for a few terms that are relevant to We.Retail activity images:

* Nature
* Outdoor 
* Sky

and notice the lack of results

2. Navigate to AEM > Assets > Files > We.Retail > English. Select the **Activities** folder and open it's properties. 

![Figure 1: Overview](images/stactivities.jpeg)

3. Check the box **Enable Smart Tags** and save the changes

4. Create a new workflow on the Activities folder and choose the **DAM Smart Tag Assets** workflow and click **Start**.

![Figure 2: Overview](images/stworkflow.jpeg)

5. Open the properties > Basic Tab for a few of the Smart Tagged assets and review the applied smart tags. 

![Figure 3: Overview](images/streview.jpeg)




## Additional Resources

[AEM Fluid Experiences for headless usecases](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-headless-usecases.html)

[AEM Content Fragments Editorial Capabilities](https://helpx.adobe.com/experience-manager/kt/sites/using/content-fragments-feature-video-use.html#editorial-capabilities)

[Downloading Content Fragments](https://helpx.adobe.com/experience-manager/kt/sites/using/content-fragments-feature-video-use.html#editorial-capabilities)

[E-Commerce API's ](https://github.com/adobe/commerce-cif-api)

[Smart Tagging ](https://helpx.adobe.com/experience-manager/6-3/assets/using/touch-ui-smart-tags.html)

## Appendix

[Experience Fragments](https://helpx.adobe.com/experience-manager/kt/sites/beta/experience-fragments-enhancements-feature-video-understand.html)

[Content Fragment Enhancements](https://helpx.adobe.com/experience-manager/kt/sites/beta/content-fragment-enhancements-feature-video-understand.html)

[Setup Adobe Stock with AEM](https://helpx.adobe.com/experience-manager/kt/assets/using/adobe-stock-aem-assets-technical-video-setup.html)

[Setup Smart Tags with AEM Assets](https://helpx.adobe.com/experience-manager/kt/assets/using/smart-tags-technical-video-setup.html)
