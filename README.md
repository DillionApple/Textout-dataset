# Textout-dataset

Text is the most important way for users to gain information. In mobile applications, many GUI components have text displayed on them. These texts function in different ways. For example, they can supply the main content, navigate users around the application and prompt them to take desired actions. However, bad text layout may cause the GUI to be messy and the text information hard to distinguish. This significantly compromises the user's experience.

The consequences of text-layout bugs are disagreeable visual issues. An obvious approach, therefore, would be to detect text-layout bugs based on the screenshots of an app during runtime.  Intuitively, we can model this problem as an image classification problem. For each image, our classifier tries to discriminate it as "normal" or "abnormal" (i.e., an image with layout bugs).

We mainly employ CNN for the image classification tasks. CNN has been proved to have a good performance on image classification tasks. But there are still many challenges to overcome. First, training a CNN generally requires thousands or even millions of images. It is easy to collect normal layout images but hard to collect a large volume of abnormal ones. This could lead to the problem of unbalanced data. Second, since a screenshot usually contains rich information and diversified data, distractions may compromise the performance of the CNN. It is also a complicated task to locate the bug areas on the screenshot precisely.

We address the challenges of text-layout bug detection as follows. To overcome the lack of abnormal data, we find a way to generate artificial abnormal data manually. We also use text detection to minimize the possibility of distraction on screenshots. This prompts the CNN to focus on text regions and reduces the risk of overfitting. It also helps us to locate the text-layout bug areas.

We propose Textout, an efficient tool to detect text-layout bugs, which is based on text detection technology and CNN. The repo contains the releases of the training dataset and the test dataset used in Textout, to facilitate future researches. And we will continuously enhance the dataset in the future.

## Dataset Releases

### 2019-8-1 v1.0 

[download](https://mega.nz/#!ClNVDQQK!d6nC874iA4TFRKZkTbDT2_DuZOb7j4W331bV7a-RZPY)

* training:
    * 580 normal screenshots
    * 33102 text-region images
        * 16551 normal text-region images
        * 16551 abnormal text-region images

* testing:
    * 59 screenshots
        * 38 normal screenshots
        * 21 abnormal screenshots
    * 1481 text-region images
        * 1405 normal text-region images
        * 76 abnormal text-region images