# -grep Commands - Isabelle Layon
> **Citation:** I researched each of these commands through prompting [ChatGPT.](https://chat.openai.com/)
## Command #1: grep -w

> Example #1
* Code Block: 
`grep -w vista berlitz1_vista.txt`


* Output:

![-w1](grep_-w_1.png)

Using `grep -w` we are able to search for a specific word inside of a file. By searching a .txt file containing all the files inside of written_2 containing
"vista", the output of this command displays the paths of the files that contain "vista" along with where the word is used. This command is useful when we need to search a large amount of files to find in which files and where inside the files a specific word is located.

> Example #2
* Code Block:
`find written_2/ | grep -w Bahamas`

* Output:

![-w2](grep_-w_2.png)

Using `grep -w` after the `find` command allows us to search for files within a directory that contain the specified word, "Bahamas", within their names. This command is useful if we are sorting files by name, or if we know that a file we are looking for contains a specific word in its name.

## Command #2: grep -c

> Example #1
* Code Block:
`find written_2/ | grep -c History`

* Output:

![-c1](grep_-c_1.png)

Using `grep -c` after the `find` command provides us with the number of times a specific word appears throughout the names of each file in a directory. In this case
the word "History" appears in 46 file names total. This command is useful when we are looking for the exact count of files a word is used inside the name of.

> Example #2
* Code Block:
`grep -c you written_2/travel_guides/berlitz2/Bahamas-History.txt`

* Output:

![-c2](grep_-c_2.png)

`grep -c` can also be used to count the number of lines a word appears in throughout a single file. In this case, the word "you" appears in Bahamas-History.txt
in 1 line. It is worth noting that if the specified word appears multiple times in a single line, the line will only be added to the count once.

## Command #3: grep -v

> Example #1
* Code Block:
`find written_2/ | grep -v History`

* Output: 

![-v1](grep_-v_1.png)

Using `grep -v` after `find` results in a list of every file inside of written_2 that does **not** contain the word "History" in its name. This command is useful for looking through files in a directory, when we know we aren't looking for any files that contain a specified word.

> Example #2
* Code Block:
`grep -v Paris written_2/travel_guides/berlitz2/Paris-WhereToGo.txt`

* Output:

![-v2](grep_-v_2.png)

`grep -v` can also be used to output each line within a file that does not contain a specified word. In this example, every line in Paris-WhereToGo.txt that does **not** contain the word "Paris" is contained in the output.

## Command #4: grep -n

> Example #1
* Code Block:
`grep -n Paris written_2/travel_guides/berlitz2/Paris-WhereToGo.txt`

* Output:

![-n1](grep_-n_1.png)

`grep -n` outputs the line number where a specified word is used in, and also outputs the contents of the line. It functions similarly to `grep -v`, however, it includes the line number and searches for when a word **is** used, rather than when it **isn't**.

> Example #2
* Code Block:
`grep -n CSE15L written_2/travel_guides/berlitz2/Portugal-History.txt`

* Output:

![-n2](grep_-n_2.png)

When attempting to search for a word that is not contained in a file, such as searching for "CSE15L" within Portugal-History.txt, `grep -n` will simply print a new line and exit back to the terminal.
