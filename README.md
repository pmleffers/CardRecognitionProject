# CardRecognitionProject
 
**By: Pieter Leffers**,

*Starting Date: September 1, 2018*

*Completion Date: - -, 2018*

*Last Updated: Nov 28, 2018*

For this overall project I wanted to pick a fairly lofty goal worthy of a lot of time put into it. My goal for this project is to identify any tournament legal Magic the Gathering card by name in real time or near real time. Inspired by other very cool card detection projects (https://github.com/geaxgx/playing-card-detection); I wanted to take the complexity of card detection to the next level.

**What makes this challenge unique?**
What sets apart this project from other card detection projects is rather than creating a model that identifies generic cards with pre-defined generic symbols (Ace of Spades,King of Hearts, Queen of Diamonds) the difficulty is creating a neural network that can distinguish over 18,000+ unique cards that have multiple printings, text changes, textures, shades, and art images. 

Below is somewhat of an example of the difficulty. We can see multiple printings of the *same card* with only one thing remaining constant, the title 'Brainstorm', even with that said a keen-eye will notice that the text is different colors for various different printings.

![alt text](https://github.com/pmleffers/CardRecognitionProject/blob/master/Brainstorms.jpg)

**Challenges**
1. Over 18,000+ unique cards
2. Multiple printings with different colors and styles
    - Different text, colors, shades, art
3. Needs to recognize the card in real-time
4. The cards may be presented against unique backgrounds and circumstances 
5. Only parts of the card may be visible

Data Source(s):
-----------
Luckily, there is a number of fantastic resources that can help me in my endeavors.

**MTG JSON**
https://mtgjson.com/

Although not the cleanest dataset MTG JSON has most printed cards by name as well as a number of juicy details such as color, mana-cost, printed card text, and sub/super-types.

**MTG Gatherer**
http://gatherer.wizards.com/Pages/Default.aspx
The MtG Gatherer has every printed card in every set style, including updated oracle texts, as well as .png images of every card I could want. This will be a fantastic resource throughout the project. 

**Scryfall**
https://scryfall.com/
Scryfall is another fantastic database with more goodies.

***Home recorded videos and images of cards***

**Additional Materials:**

* http://colah.github.io/posts/2015-08-Understanding-LSTMs/

* https://www.kdnuggets.com/2018/09/object-detection-image-classification-yolo.html#.W5bJ1wFKfgI.linkedin

* https://www.pyimagesearch.com/2018/09/17/opencv-ocr-and-text-recognition-with-tesseract/?__s=bir9h53nkfqssqsteipg

* https://www.pyimagesearch.com/2018/08/20/opencv-text-detection-east-text-detector/

* https://github.com/geaxgx/playing-card-detection

* https://github.com/AlexeyAB/darknet#how-to-train-to-detect-your-custom-objects

Part 1: The Subgame
================
For this foundation part of the project I create videos to use for object detection, identifying cards within videos, capturing them in images, and storing card images into a created file structure on the system. After that is complete I sample random cards and identify portions for detection of unique elements, then overlay multiple cards on a randomly generated background to be used for training a neural network.

Here is an example of the data source I used for this part of the project:

[![Youtube card video](https://github.com/pmleffers/CardRecognitionProjectPart1/blob/master/YoutubeThumb.jpg)](https://www.youtube.com/watch?v=uHIOnX9ktjs)

[More description is provided in the Jupyter Notebook.](http://nbviewer.jupyter.org/github/pmleffers/CardRecognitionProjectPart1/blob/master/MtG_Card_Recognition_Subgame.ipynb)

Update: 2/2/2019
================
* Need to increase framerate
* Add skip frames
* Modify it to index card names 

[![Youtube card video](https://github.com/pmleffers/CardRecognitionProjectPart1/blob/master/YoutubeThumb.jpg)](https://www.youtube.com/watch?v=tTXB3zKv8iU&feature=youtu.be)
