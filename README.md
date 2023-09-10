# Poetry Generator

This repository contains a Python notebook that utilizes the Markov model to generate poetry based on a collection of poems by Robert Frost. The Markov model implemented here includes both first and second-order dependencies, allowing the generated text to have a richer context and structure.

## Markov Model

The Markov model is a statistical approach used to describe sequences of events where the probability of the next event depends solely on the current state and is independent of past states. In simpler terms, it's a way to model how one event leads to another without considering the entire history of events.

The core components of a Markov process include:

* States: A finite set of possible states, often represented by letters, numbers, or names.

* Transition Matrix: A matrix that represents the transition probabilities between states. Each element (i, j) of the matrix represents the probability of transitioning from state i to state j in a single step.

In this notebook, we apply the Markov model to generate poetic lines based on the text of Robert Frost's poems.

## Functions

`clean_text_and_tokenize(text)`
This function takes a text input and performs the following tasks:

* Removes punctuation.
* Converts text to lowercase.
* Splits the text into individual words.

`Add2Dict(dict_, key, value)`
This function checks if an element is present in a dictionary. If not, it creates the element and adds the specified value to it.

`List2ProbDict(word_list)`
This function calculates the probability of each element based on its distribution in a list. It returns a dictionary where each element is associated with its probability.

## Sampling and Generation
The `SampleWord(probability_dict)` function selects a word based on its probability distribution. This is used in the generation of poetry.

`GenerateText()`
This function generates poetry using the Markov model. It starts with an initial word, samples the next words based on the model, and continues until an "END" token is encountered or until the desired number of lines (`LINES`) is generated.

## Example Output
Here's an example of poetry generated using this notebook:

```
but estelle dont complain shes like him there
ill double theirs for both of them
she hadnt found the fingerbone she wanted
```

Feel free to explore and experiment with the code to generate your own poetic creations inspired by Robert Frost's works.
