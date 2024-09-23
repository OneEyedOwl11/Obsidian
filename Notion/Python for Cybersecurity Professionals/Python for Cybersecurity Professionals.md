- 1.1 Course Intro
    
    it’s an intro \(0_0)/
    
- 1.2 Setting up environment
    
    replit.com
    
      
    
- 1.3 Hello World!
    
    it’s hello world and variable
    
    x = insertVariableHere
    
- 1.4 Working with strings
    
    concatinate strings and use multi-line strings
    
    input prompt
    
- 1.5 other types of variables
    
    int and float
    
- 1.6 Passing command line arguments
    
    Use “python3” to run python library
    
    arguments are anything after the initial argument eg “python3”
    
    index 0 is 1st argument and second is 1
    
      
    
- 1.7 Basic logic and algorithms 1 & 2
    
    write down psuedo code before writing actual code so you can plan out what you’re doing
    
    use real coding statements to describe what you need
    
    eg if, for, while & etc
    
      
    
- 1.9 If Statements
    
    you’ve gone through this
    
      
    
- 1.10 For Loops
    
    ```Python
    cars = ["toyota","honda","ford","chevrolet"]
    
    for x in cars:
      if x == "toyota":
        print("this car is on sale: " + x)
      else:
        print(x)
    ```
    
- 1.11 Recursion
    
    ```Python
    def countingDown(x):
      if x > 0:
        print(x)
        countingDown(x - 1)
      else:
        print(x)
      
    
    x = -3
    countingDown(x)
    ```
    
- 1.12 While Loops
    
    most recursive statements can be used here to use less RAM
    
      
    
- 1.13 Recursion 2
    
    when there are special edge cases it would be better to use recursion rather than use a while statement
    
    eg when going down a number list you would need another
    
- 2.1 Takin CSV Input
    
    CSV = Comma separated Values
    
    use the built in csv reader in python
    
    ```Python
    import csv
    
    with open('test.csv') as csv_file:
      csv_reader = csv.reader(csv_file, delimiter=',')
      line_count = 0
      for row in csv_reader:
        if line_count == 0:
          print(f'the headers are {", ".join(row)}')
          line_count += 1
        else:
          print(f'\t{row[0]} is taking classes on {row[1]}and has completed {row[2]} most recently.')
    ```
    
    ```Markdown
    name,platform,recent_course
    imran, cybrary,python for security pros
    john, cybrary, intro to security
    ```
    
- 2.2 Lists
    
    for loop through a list
    
    ```Python
    for letter in testList:
      print(letter)
    ```
    
    See if something is in a list
    
    ```Python
    if "b" in testList:
      print("it's here")
    else:
      print("Womp Womp.")
    ```
    
    while loop through a list
    
    ```Python
    while i < len(testList):
      print(testList[i])
      i += 1
    ```
    
    add to end of list
    
    ```Python
    testList.append('e')
    
    print(testList)
    ```
    
    remove from list
    
    ```Python
    testList.remove('')
    ```
    
    insert data to an index of a list
    
    1st argument is index and second is the data you want to insert
    
    ```Python
    testList.insert(1, 'b')
    ```
    
- 2.3 Dictionaries
    
    Access data from the key and read data from there.
    
    lists you’d just access the index
    
    rainbow table = a list of passwords and their hash’s
    
    you need the key to access the data (also acts as a form of security)
    
    code for lesson
    
    ```Python
    dict = {}
    dict['a'] = 'alpha'
    dict['b'] = 'beta'
    dict['c'] = 'ceta'
    print(dict['b'])
    
    dict['b'] = 'new beta'
    
    print(dict['b'])
    
    for key in dict:
      print(dict[key])
    
    print(dict.keys())
    print(dict.values())
    ```
    
- 2.4 Sets
    
    initialize like dictionaries. set data like lists
    
    sets are unordered
    
    more secure because it’s harder to change data in a set
    
    set deletes duplicate data
    
    code used
    
    ```Python
    sampleset = {'hello','friends','from','cybrary'}
    
    sampleset2 = set(('this','is','a','course', True, 5))
    
    print(sampleset2)
    ```
    
- 2.5 Tuple
    
    tuples are ordered and unchangeable and indexable
    
    allow duplicate values
    
    if tuple has one value put comma after it (standard practice)
    
- good graph for data types
    
    ![[Untitled 2.png|Untitled 2.png]]
    
    ![[Untitled 1 2.png|Untitled 1 2.png]]
    
- 3.1 More about ciphers
    - symmetric key
        
        uses a key to encrypt data
        
        they key to encrypt or decrypt are the same
        
        usually uses some sort of cypher
        
    - asymmetric key
        
        person sending and person receiving have different keys
        
        anyone can send you encrypted data using your public key which would then require you to decrypt it using your private key
        
    - hash function
        
        math problems tht your data goes through to be encrypted or decrypted eg SHA256
        
    - transposition cipher
        
        changes the position of characters without actually changing the characters themselves
        
    - code used for transposition cypher
        
        ```Python
        def encrypt(key, message):
          ciphertext = [''] * key
          for x in range(key):
            pointer = x
        
            while pointer <len(message):
              ciphertext[x] += message[pointer]
              pointer += key
          return ''.join(ciphertext)
        
        
        def main():
          message = input('enter a message: ')
          key = int(input('select a key'))
          print(encrypt(key, message))
        
        
        if __name__ == '__main__':
          main()
        ```
        
- 3.2 Working with PIP
    
    pypi.org
    
    use this site to install packages that are related to what you’re working on
    
- 3.3 Keylogger
    
    ```Python
    from getkey import *
    from datetime import datetime
    now = datetime.now()
    
    while True:
      key = getkey()
      print(key)
    ```
    
    https://github.com/D4Vinci/PyLoggy
    
- 3.4 Packet Sniffer
    - this is a packet
        
        ![[Untitled 2 2.png|Untitled 2 2.png]]
        
    - sniffer
        
        [Packet-Sniffer/sniff-it.py at master · shreyasgune/Packet-Sniffer · GitHub](https://github.com/shreyasgune/Packet-Sniffer/blob/master/sniff-it.py)
        
    - resources
        
        docs.python.org/3
        
        hackerrank.com/domains/python
        
        leetcode.com