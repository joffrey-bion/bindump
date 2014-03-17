BinDump
=======

A binary file dumper. This is a simple program to display the bits of a binary file. Especially useful to debug encoding programs.

### Usage

`java com.jbion.bindump.BinDump <filename> [nbBytesPerLine]`

Or using the provided runnable JAR file:

`java -jar BinDump.jar <filename> [nbBytesPerLine]`

### Example

Here is an example of a short UTF-8 text file named `testfile.txt`:
```
abcdefg
```

Here is how to dump it with BinDump (no option):
```
java -jar BinDump.jar testfile.txt
```

Output:
```
Reading in binary file named : testfile.txt
File size: 10
11101111
10111011
10111111
01100001
01100010
01100011
01100100
01100101
01100110
01100111
Num bytes read: 10
```

#### Bytes per line option

If 1 byte per line produces too many lines, you may add the number of bytes per line as a second argument:
```
java -jar BinDump.jar testfile.txt 2
```

Output:
```
Reading in binary file named : testfile.txt
File size: 10
1110111110111011
1011111101100001
0110001001100011
0110010001100101
0110011001100111
Num bytes read: 10
```
