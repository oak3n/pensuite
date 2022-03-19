# the `ls` command
## install
you already have it

## use
###list file details
`ls -lisan file.foo`

### flags
- *l:* request long listing format when printing. more info
- *i:* appends inode number of the file to results
- *s:* prints the file size in blocks
- *a:* prints out all entries and does not ignore any files
- *n:* prints out the numeric user id and group id
- *h:* print the siezes in the human readable format

###`locate` file and pipe output into `ls` for more info
`locate image.jpg | xargs ls -h`


## links
- [some blog post](https://www.lostsaloon.com/technology/how-to-view-all-details-or-metadata-of-a-file-in-linux-command-line/)
