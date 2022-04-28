Print file values:
`cat <file_name> | head`

Print field 20 with '|' as delimiter:
`cat <file_name> | cut -d'|' -f20`

Print multiple fields (20,34) with '|' as delimiter:
`cat <file_name> | cut -d'|' -f20,34`

Count lines in a file:
`wc -l <file_name>`

Count number of unique data sorted by a single field:
`cat <file_name> | cut -d'|' -f20 | sort | uniq | wc -l`

Count number of unique data sorted by multiple fields (20,34):
`cat <file_name> | cut -d'|' -f20,34 | sort | uniq | wc -l`

Print total numbers of columns with '|' as delimiter:
`awk '{FS="|"}; {print NF}' <file_name> | sort -nu | tail -n 1`

(https://linuxize.com/post/linux-cut-command/)