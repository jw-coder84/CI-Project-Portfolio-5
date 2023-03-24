# Cherry Leaves Mildew Detection

## Dataset Content
* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/cherry-leaves). We then created a fictitious user story where predictive analytics can be applied in a real project in the workplace.
* The dataset contains +4 thousand images taken from the client's crop fields. The images show healthy cherry leaves and cherry leaves that have powdery mildew, a fungal disease that affects many plant species. The cherry plantation crop is one of the finest products in their portfolio, and the company is concerned about supplying the market with a compromised quality product.


## Business Requirements

* 1 - The client is interested in conducting a study to visually differentiate a healthy cherry leaf from one with powdery mildew.
* 2 - The client is interested in telling whether a given cherry leaf is covered with powdery mildew or not.


## Hypothesis and how to validate?
* We suspect cherry leaves can be identified as being healthy or having powdery mildew. 
* The powdery mildew is white so is easily identifiable against the green of the leaf.


## The rationale to map the business requirements to the Data Visualisations and ML tasks

* Business Requirement 1: Data Visualization

   * We will display the "mean" and "standard deviation" images for healthy and mildew leaves.
   * We will display the difference between an average healthy leaf and an average mildew leaf.
   * We will display an image montage for either healthy or mildew leaves.

<br>

* Business Requirement 2: Classification

   * We want to predict if a given cherry leaf is healthy, or has powdery mildew.
   * We want to build a binary classifier and generate reports.



## ML Business Case

The cherry plantation crop from Farmy & Foods is facing a challenge where their cherry plantations have been presenting powdery mildew. Currently, the process is manual verification if a given cherry tree contains powdery mildew. An employee spends around 30 minutes in each tree, taking a few samples of tree leaves and verifying visually if the leaf tree is healthy or has powdery mildew. If there is powdery mildew, the employee applies a specific compound to kill the fungus. The time spent applying this compound is 1 minute.  The company has thousands of cherry trees, located on multiple farms across the country. As a result, this manual process is not scalable due to the time spent in the manual process inspection.

To save time in this process, the IT team suggested an ML system that detects instantly, using a leaf tree image, if it is healthy or has powdery mildew. A similar manual process is in place for other crops for detecting pests, and if this initiative is successful, there is a realistic chance to replicate this project for all other crops. The dataset is a collection of cherry leaf images provided by Farmy & Foods, taken from their crops.


## Dashboard Design

### Page 1: Quick Project Summary
* Quick project summary
	* General Information
      * The client is interested in conducting a study to visually differentiate a cherry leaf that is healthy from one that contains powdery mildew. The client is interested in predicting if a cherry leaf is healthy or contains powdery mildew.

      * Mildew is a white covering over the leaves that can be wiped off with the fingers. In extreme cases, it should be brought under control. The client does not want to supply the market with a product of compromised quality.


### Page 2: Cherry Leaf Visualizer
* It will answer business requirement 1
	* Checkbox 1 - Difference between average and variability image
	* Checkbox 2 - Differences between average healthy and average mildew covered leaves
	* Checkbox 3 - Image Montage

### Page 3: Mildew Detector
* Business requirement 2 information - "The client is interested in telling whether a given cherry leaf is covered with powdery mildew or not."
* Link to download a set of cherry leaf images for live prediction.
* User Interface with a file uploader widget. The user should upload multiple cherry leaf images. It will display the image and a prediction statement, indicating if the cherry leaf is covered with powdery mildew or not and the probability associated with this statement. 
* Table with the image name and prediction results.
* Download button to download table.

### Page 4: Project Hypothesis and Validation
* Block for each project hypothesis, describe the conclusion and how you validated it.

### Page 5: ML Performance Metrics
* Label Frequencies for Train, Validation and Test Sets
* Model History - Accuracy and Losses
* Model evaluation result


* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other items, that your dashboard library supports.
* Finally, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project, you were confident you would use a given plot to display an insight, but later, you chose another plot type).

## Deployment
### Heroku

* The App live link is: https://leaf-mildew-detection-data.herokuapp.com/
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file. 


## Main Data Analysis and Machine Learning Libraries
The following libraries were used for this project:

* numpy
   * Calculating the mean and variability of images per label (healthy / powdery mildew).
   * Determine the difference between images of the average healthy and average powdery mildew leaves.
   * Expand the shape of an array when converting the image to an array for predicitons.

* pandas
   * A data frame was used to organise the data which was used to plot the number of images, in the train, test and validation sets.
   * The ML model history was stored in a data frame to plot the model performance stats.

* matplotlib and seaborn
   * Plot the height and width of the images.
   * Plot the mean and variability of images per label (healthy / powdery mildew)
   * plot the difference between images of the average healthy and average powdery mildew leaves.
   * Generate the image montage for each label.
   * Plot a bar graph to show the number of images in the train, test and validation sets.
   * Plot showing the augmented images in the train, validation and test sets.
   * Plot a line graph showing the ML models learning curve. One for validation loss and one for accuracy.

* streamlit
   * Streamlit was used to create the dashboard to provide a user interface where the client can access various parts of the project. This includes written information, Jupiter Notebook code output, and the ability to upload new images to test the ML algorithm.

* tensorflow-cpu and keras
   * Pre-processing of images for the average variability task.
   * Augment image data in train, validation and test sets.
   * Creating the ML model neural network. The Sequential model is used as each layer of the neural network has one input and one output. The following layers were used in the nerual network: Activation, Dropout, Flatten, Dense, Conv2D, MaxPooling2D.


## Credits 

* In this section, you need to reference where you got your content, media and from where you got extra help. It is common practice to use code from other repositories and tutorials. However, it is necessary to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- I used a description of cherry leaf mildew from the following site: http://www.tree-guide.com/cherry-leaves

### Media


## Acknowledgements (optional)
* Thank the people that provided support throughout this project.
