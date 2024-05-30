# ops201-opschallenge6

Ops Challenge - Conditionals
Overview
Conditionals allow your script to test whether a situation is true and then proceed accordingly.

Objectives
Create a script that detects if a file or directory exists, then creates it if it does not exist.
Your script must use at least one array, one loop, and one conditional.


#!/bin/bash

# Define an array of file names
filenames=("rap.txt" "country.txt" "rock.txt")

# Loop through each filename in the array and check if it exists
for filename in "${filenames[@]}"; do
    if [ -e "$filename" ]; then
        echo "$filename exists."
    else
        # Create the file if it does not exist
        touch "$filename"
        echo "$filename has been created."
    fi
done
