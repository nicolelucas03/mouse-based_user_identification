## Exploring Mouse-Based User Identification
**Co-Author**: Nicole Lucas

**Email**: nicoleclucas003@gmail.com 

### Tools Used :hammer_and_wrench: 
- **Python**
- **Jupyter Notebook**
- **LaTeX**
  
### Goal :dart:
The goal of our research project is to investigate the feasibility of using mouse movement patterns as a method for uniquely identifying individual users on a webpage. Specifically, we aim to analyze multiple aspects of mouse behavior, including movement velocity, trajectory, frequency of clicks, and hover patterns to determine if these elements can be used as distinctive biometric identifiers. Unlike traditional tracking methods such as IP-based identification or cookies which often raise privacy concerns, mouse movement analysis offers an alternative that respects user anonymity while still participating in behavior-based identification. This research will also focus on handling the inherent noise in the collected mouse movement data. Due to factors such as variability in user interactions, device types, and even environmental conditions, mouse movements are accompanied by random fluctuations that can obscure meaningful patterns. As part of our research, we will explore techniques for filtering and processing this noise to enhance the accuracy and reliability of user identification. Ultimately, this research seeks to determine whether mouse movement patterns, despite their noisy nature, can provide a reliable means of identifying users across different browsing sessions or web pages

### Research Questions :question:
- Can mouse movement patterns, including speed, direction, and frequency, be utilized as reliable biometric identifiers for individual users across different web pages? 
- How do external factors such as device type, screen resolution, and browser influence the consistency and uniqueness of mouse movement patterns for user identification? 
- What techniques are most effective in isolating distinctive mouse movement features from noise to most accurately identify users? 
- How much variability in user behavior can be tolerated before it directly impacts the accuracy of user identification? 
- Can mouse movement-based tracking provide a viable alternative to other traditional tracking methods in terms of both user identification accuracy and privacy preservation?

### Methods :notebook:
In general, webpages can see mouse movements of the user when the page is in focus. To test whether this mouse data can be used for the fingerprinting and thus tracking of users, we must aim to identify the potential uniqueness of mouse data. First, JavaScript event listeners can be utilized to extract exact mouse movement, scrolling, and clicking data. This raw data can be stored as coordinates with timestamps to allow for further processing. In order to mitigate the effects of noisy movements such as random jitters and micro-adjustments or other involuntary movements, we can pre-process the data before we can look at it with smoothing filters such as Savitzky-Golay filter and other basic filtering of extraneous data. Next, specific, potentially unique features can be constructed from the data such as average speed, average acceleration, average jitter, lingering time, hesitation time, pathing behavior, and scroll behavior can be computed from the raw mouse data. This data then can be passed initially through an unsupervised model, and if viable, a supervised machine learning model to determine whether a user can be classified based off its mouse behaviors. The unsupervised model, such as DBScan, can be used as a baseline to identify clusters of similar mouse data and determine whether a specific user’s mouse data can be generally unique. This will determine the viability of training the more advanced supervised model like a random forest or neural network, to be able to, with a user’s complex mouse data, both identify a user explicitly and track a user across sessions. The resultant supervised model’s performance metrics (accuracy, precision, recall, and f1-score) will then be used to determine the real-world performance of such a model in fingerprinting users across the web.


### Read the Paper! :newspaper:
Read the [full paper](https://nicolelucas03.github.io/personal_website/docs/MouseBasedIdentification.pdf) written by myself, Lev Rose, and Mohammed Rouie Miab. 




