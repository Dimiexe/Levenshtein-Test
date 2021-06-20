# Levenshtein-Test
This code is a specific implementation for the given instructions (specifically, only for Levenshtein distance of 1) and I considered that a generalised implementation for any distance is not desired. However, if you would like to see a more scalable approach, I would welcome the challenge :)

I took a look in the data and noticed many names in quotes, having a second name in parenthesis, having a form like: "foo v. fee", or in all uper-case letters. No special treatment was designed for those names and EVERY name in the dataset was processed as if that cell contained only the characters making up the name of the Hund. So for example if a name was "Luc" it was treated as a 5 character long name and was discarded right away, even though Luc (the actual name) has a Levenshtein distance of 1 from Luca.

Finally, I want to make clear that only names with a Levenshtein distance of 1 from "Luca" were detected, so any instances of the exact same name "Luca" (distance 0) were discarded.
