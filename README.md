# DataMiningChallenge20202
Determine the gender of Reddit authors using their comments

(https://www.kaggle.com/c/datamining2020/overview/evaluation)

*Reddit is an entertainment, social networking, and news website where registered community members can submit content, such as text posts or direct links, making it essentially an online bulletin board system. Registered users can then vote submissions up or down to organize the posts and determine their position on the site's pages. Content entries are organized by areas of interest called "subreddits". The subreddit topics include news, gaming, movies, music, books, fitness, food, and photosharing, among many others.*
*The Reddit website has an API and its code is open source. In July 2015, a Reddit user identified as Stuck_In_the_Matrix made public a dataset of Reddit comments for research. The dataset has approximately 1.7 billion comments and takes 250 GB compressed. Each entry contains comment, score, author, subreddit, position in comment tree and other fields that are available through Reddit's API.*
One of the user attributes that is not natively supported by the Reddit platform is the gender. However, in some subreddits, users can self report their genders as part of the subreddit rules. In the scope of this competition, users that self reported their gender are selected from the dataset, and **your goal is to predict the gender of these users**.

The **evaluation metric for this competition is the Area Under the ROC Curve**. This metric is used to evaluate binary classification, and in the scope of this competition we are representing the gender of the users as binary classes: the class "female" is represented as 1 and the class "male" as 0. The class prediction for each Reddit author corresponds to your confidence that the author is a female, which is a "score" computed for the author (e.g. estimated probability in logistic regression).

*Submission Format:*
For every author in the dataset, submission files should contain two columns: author and gender. The column author should be a string. The column gender can be any real value. The higher is your confidence that the author is female, the higher should be the corresponding value in the gender column.
 
 
 The notebook is composed by five parts:
1. Load data and EDA
2. Preprocessing
3. Feature matrix creation (with doc2vec, tdidf, sparse matrix)
4. Training and evaluation for model selecion
5. Retrain over the whole dataset + prepare the solution
