# INSPIRED2 Dataset

Here we have two directories for two different formats of the dataset .

1. The first directory named 'json' contains dataset in the form of JSON.
2. The other directory named 'tsv' contain dataset in the form of Tab-separated Value (TSV) as was reported originally. 

Apart from two directories, a file named 'movie_database.tsv' includes movie titles and corresponding meta-data entities for items mentioned in the INSPIRED2 dataset.

## Dataset Statistics
Overall, the INSPIRED2 dataset includes 1,001 dialog between paired human-recommenders and human-seekers. As per the original work, the dataset is splitted with 8:1:1 in three different sets, i.e., train, dev, and test, respectively.

## Dataset Features (columns)
We elaborate on the features of the INSPIRED2 dataset as follows.


1. `dialog_id`: unique dialog id for each conversation
2. `utt_id`: unique utterance id for each utterance in a particular dialog
3. `speaker`: role of the speaker, i.e., either a human-recommender or human-seeker
4. `turn_id`: turn id for each human-recommender and seeker utterance pair
5. `text`: complete utterance without annotations 
6. `text_with_placeholder`: complete utterance where the movie titles and meta-data entities (genre, actor's name, director's name, movie plot) have been replaced with 7.  the corresponding placeholder. 
8. `movies`: list of movie titles mentioned in a particular utterance
9. `genres`: list of genres mentioned in a particular utterance
10. `people_names`: list of people's like cast, actors, directors, etc., names mentioned in a particular utterance
11. `movie_dict`: a dictionary that contains all the titles mentioned in a particular dialog (as keyes) paired with its corresponding index
12. `genre_dict`: a dictionary that contains all the genres in a particular dialog (as keyes) paired with its corresponding index
13. `actor_dict`: a dictionary that contains all the actors's names mentioned in a particular dialog (as keyes) paired with its corresponding index
14. `director_dict`: a dictionary that contains all the directors' names mentioned in a particular dialog (as keyes) paired with its corresponding index
15. `others_dict`: a dictionary that contains each person's name (apart from actor and director) in a particular dialog (as the key) paired with its corresponding index
16. `first_label`: main sociable strategy labelled explicitly
17. `second_label`: this is the second strategy (optional)
18. `fine_label`: a label that denotes for one of the five cases whether the seeker accepted or rejected the recommendation.
	* accept_rating_good: user accepted the recommendation and later rated the recommended movie with the score 4 or 5
	* accept_rating_mod: user accepted the recommendation and later rated the recommended movie with the  score <= 3
	* accept_uninterested: user accepted the recommendation, didn't finish watching the trailer, and later said that they found the trailer uninteresting
	* accept_others: user gave various reasons for not finishing the trailer
	* reject: user rejected the recommendation
19. `movie_id`: unique movie id recommended by the human-recommmender. for the trailer, replace "XXX" in this link https://www.youtube.com/watch?v=XXX with the movie id
