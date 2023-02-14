# -grep Commands - Isabelle Layon
## Command #1: -w
> Source: Asking ChatGPT

> Example #1
* Code Block: 
`grep -w vista berlitz1_vista.txt`


* Output:

Using `grep -w` we are able to search for a specific word inside of a file. By searching a .txt file containing all the files inside of written_2 containing
"vista", the output of this command displays the paths of the files that contain "vista" along with the exact place the word is used. This command is useful when we need
to search a large amount of files to find in which files and exactly where a specific word is located.

> Example #2
* Code Block:
`find written_2/ | grep -w Bahamas`

* Output:

Using `grep -w` after the `find` command allows us to search for files within a directory that contain the specified word, "Bahamas", without the need for creating a
new .txt file. It however differents from the first example in that the exact sentence the word is used in each file is not in the output, therefore this command is
more useful if we are not specifically looking for where in the files the word is used.

## Command #2: -c
> Source: Asking ChatGPT

## Command #3: -v
> Source: Asking ChatGPT

## Command #4: -n
> Source: Asking ChatGPT
