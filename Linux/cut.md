The cut command in Linux is used to extract sections from each line of text in a file or piped data. It can be used to cut by byte position, character, and field (column), based on a delimiter. Here’s a brief explanation of how to use it:

# Syntax:
cut [OPTION]... [FILE]...

OPTION specifies the behavior of the cut (e.g., -b for bytes, -c for characters, -f for fields).
FILE represents the input file(s). If no file is specified, cut reads from standard input.

# Options:
    -b: Selects only the bytes specified in a list (e.g., -b 1-3,7).
    -c: Selects only the characters specified in a list (e.g., -c 1-3,7).
    -d: Specifies a delimiter to use instead of the default tab delimiter.
    -f: Selects only the fields specified in a list, separated by the delimiter (e.g., -f 1,3).
    --complement: Inverts the selection, displaying all bytes, characters, or fields except the selected ones.
# Examples:
    To extract the first three characters of each line from a file:
    cut -c 1-3 filename

    To extract the second and fifth fields of each line using a comma as a delimiter:
    cut -d ',' -f 2,5 filename
