To classify SMS messages as spam or legitimate, we followed a process with the power of machine learning:

1) Understanding the Data: 
  We started with a dataset containing thousands of SMS messages, each labeled as either "spam" or "ham" (legitimate). Just like a person might notice that spam messages often mention prizes or urgent actions, we wanted our model to pick up on these patterns

2) Cleaning and Preparing the Messages:
  Since computers don't understand language like we do, we had to make the messages "machine-readable." This meant:
  - Converting all text to lowercase so "WIN" and "win" are seen as the same
  - Removing punctuation and special characters to focus on the words themselves
  - Breaking sentences into individual words (tokenization)
  - Removing common words like "the" or "is" that don't help distinguish spam from legitimate messages (stop words)
  - Reducing words to their root forms, so "winning" and "win" are treated equally (stemming)

 3) Turning Words into Numbers:  
  Because machine learning models work with numbers, we used a method called TF-IDF. This technique assigns higher importance to words that are unique to a message (like "prize" in spam), and less to words that appear everywhere (like "hello")[2][4]. This is similar to how a person might pay more attention to unusual words when judging if a message is suspicious.

4) Exploring the Data:
  We visualized the distribution of spam and legitimate messages, noticing that spam messages are much less frequent—a situation called class imbalance. We also looked at the most common words in each category, finding that spam often includes terms like "free," "win," and "urgent"

6) Training the Model:
  The dataset was split into two groups: one for teaching the model (training) and one for testing its skills (testing). We tried out different algorithms—Naive Bayes, Logistic Regression, and Support Vector Machines—each learning from the patterns in the training messages

7) Evaluating Performance:
  After training, we tested the models on new, unseen messages to see how well they could identify spam. We measured their accuracy and looked at confusion matrices to understand where they made mistakes—just like a person might review their own sorting to improve next time

8) Key Takeaways:
  The best models could spot spam with high accuracy, often above 97%[3][4]. The process combined human-like intuition (spotting suspicious words and patterns) with mathematical rigor, allowing the AI to quickly and reliably filter out unwanted messages.

In summary, we cleaned and transformed the text so a computer could understand it, taught a model to recognize the difference between spam and legitimate messages, and checked its work—much like a careful human would, but at a much larger scale and speed.
