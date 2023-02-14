# -grep Commands - Isabelle Layon
> **Citation:** I researched each of these commands through asking [ChatGPT.](https://chat.openai.com/)
## Command #1: grep -w

> Example #1
* Code Block: 
`grep -w vista berlitz1_vista.txt`


* Output:

Using `grep -w` we are able to search for a specific word inside of a file. By searching a .txt file containing all the files inside of written_2 containing
"vista", the output of this command displays the paths of the files that contain "vista" along with the exact place the word is used. This command is useful when we need to search a large amount of files to find in which files and exactly where a specific word is located.

> Example #2
* Code Block:
`find written_2/ | grep -w Bahamas`

* Output:

Using `grep -w` after the `find` command allows us to search for files within a directory that contain the specified word, "Bahamas", without the need for creating a
new .txt file. It however differents from the first example in that the exact sentence the word is used in each file is not in the output, therefore this command is
more useful if we are not specifically looking for where in the files the word is used.

## Command #2: grep -c

> Example #1
* Code Block:
`find written_2/ | grep -c History`

* Output: 

Using `grep -c` after the `find` command provides us with the number of times a specific word appears throughout the names of each file in a directory. In this case
the word "History" appears in 46 files total. This command is useful when we are looking for the exact count of files a word is used inside the title of.

> Example #2
* Code Block:
`grep -c you written_2/travel_guides/berlitz2/Bahamas-History.txt`

* Output: 

`grep -c` can also be used to count the number of lines a word appears in throughout a single file. In this case, the word "you" appears in Bahamas-History.txt
in 1 line. It is worth noting that if the specified word appears multiple times in a single line, the line will only be added to the count once.

## Command #3: grep -v

> Example #1
* Code Block:
`find written_2/ | grep -v History`

* Output: 

Using `grep -v` after `find` results in a list of every file inside of written_2 that does **not** contain the word "History" in its name. This command is useful for looking through files in a directory, when we know we aren't looking for any files that contain a specified word.

> Example #2
* Code Block:
`grep -v Paris written_2/travel_guides/berlitz2/Paris-WhereToGo.txt`

* Output:

`grep -v` can also be used to output each line within a file that does not contain a specified word. In this example, every line in Paris-WhereToGo.txt that does **not** contain the word "Paris" is contained in the output.

## Command #4: grep -n

> Example #1
* Code Block:
`grep -n Paris written_2/travel_guides/berlitz2/Paris-WhereToGo.txt`

* Output: 

`grep -n` outputs the line number where a specified word is used in, and also outputs the contents of the line. It functions similarly to `grep -v`, however, it includes the line number and searches for when a word **is** used, rather than when it **isn"t**.

> Example #2
* Code Block:
`grep -n CSE15L written_2/travel_guides/berlitz2/Portugal-History.txt`

* Output:

When attempting to search for a word that is not contained in a file, such as searching for "CSE15L" within Portugal-History.txt, `grep -n` will simply print a new line. 
