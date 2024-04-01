what is sed command in linix? 
<s>How to use the sed command in Linux for replacing text within a file with another text.

Answer: The `sed` (Stream Editor) command in Unix/Linux is an extremely powerful tool that can be used to perform various text manipulations.
[vagrant@localhost ~]$ vim sample
    Sed Command 101: Mastering the Basics for Efficient text Editing
    Unleashing the Power of Sed: Advanced Techniques for Streamlining Your Workflow
    Sed Command Demystified: A Comprehensive Guide for text Processing
    Boost Your Productivity with Sed Command: Tips and Tricks for Success
    Sed Command Secrets: Unlocking Hidden Features for text Manipulation 
    :wq
    [vagrant@localhost ~]$ sed 's/Command/Instruction/g' sample
    it'll print the file with the replacing text, but not actually change it unless we provide the option -i

    [vagrant@localhost ~]$ sed -i 's/Command/Instruction/g' sample
    
### sed '/^ *$/d' inputFileName
The above example uses a few of the below regular expression metacharacters:

    The caret (^) is the same as the starting of the line.
    The dollar symbol ($) is the same as the completion of the line.
    The asterisk (*) is the same as the more or zero previous character occurrence.
    The plus symbol (+) is the same as the one or multiple previous character occurrences.
    The question mark (?) is the same as the more or zero previous character occurrence.
    The dot symbol (.) is exactly the same as one character.
    So, "sed '/^ *$/d'" will delete all empty lines from your document. 

### Substituting Multiple Words Using SED
To replace two words at once using `sed`, you can chain the substitution commands like this:
bash $ echo "Hello World" | sed 's/Hello/Goodbye/; s/World/Moon/'
Goodbye Moon
### Print only part of a Line With SED
If you want to print only part of a line that matches a pattern, you can use the following format:
bash $ echo "I love coding" | sed 's/love/eat/'
I eat coding
