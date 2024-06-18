# Heredity
This is a project made in Python and submitted for the CS50 AI Harvard course. This AI uses a Bayesian Network to determine the conditional probability that a person exhibits a specific trait. The machine may or may not be given pieces of information, like whether or not the parents have the trait, to determine the likelyhood that the person has 0, 1, or 2 copies of the gene, and also whether or not the person exhibits the trait. The numbers currently represent the probabilities for a mutation in the GIB2 gene and whether or not the hearing loss trait is shown.

## Setup

a file, family0.csv, can be found in /data/ containing a sample family, but any other csv text files can be added. 

To run, pass the csv file into args[0] like this: 
    
    python heredity.py data/[FILENAME].csv

For any file added, format it like this

The first line in the file must be: name,mother,father,trait

After that, each line represents a person, and the data inputted should follow the above instructions (name, mother's name, father's name, 1 if have trait, 0 if not). Make sure it is separated by commas

Each person must have a name, but they may or may not have a known mother/father and it may or may not be known if they have the trait. If any information is not known, leave it blank

NOTE: it only works if BOTH OR NEITHER mother and father are known. It does not work if a mother is known but father isn't or vise versa.

In the example file, it is formatted like this:

    name,mother,father,trait
    Gary,Maria,John,
    John,,,0
    Maria,,,1

  As seen, Gary has Maria and John as a mother, but it is unknown whether he has the trait (it is blank)

  John's parents are not included, so their slots are empty, but still separated by commas


## Modifications

in heredity.py, the values of PROBS can be modified if you would like to change the gene being tracked, or to mess around with different numbers.

"gene" represents the probability you have 0, 1, or 2 copies of the gene given you have no known parents

"trait" represents the probability that you have/do not have the associated trait given that you have 0, 1, or 2 copies of the gene

"mutation" represents the probability that you gain or lose a copy of the gene due to a mutation
