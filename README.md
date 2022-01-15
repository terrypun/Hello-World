# Hello-World
This may be where i make initial additions.

may add a whole python program

## crytogram helper
temp_num = '20'


## fix patterns to exclude words with letters we know are not in it
import quote_reader
import crypto_word_finder_module
import string
the_code = "VB OAM CTGL ZAJDLPVGY ZTV, TZI T JTG, VB OAM CTL ZAJDLPVGY HAGD, TZI T CAJTG. - JTNYTNDL LPTLUPDNVB OAM CTGL ZAJDLPVGY ZTV, TZI T JTG, VB OAM CTL ZAJDLPVGY HAGD, TZI T CAJTG. - JTNYTNDL LPTLUPDN"
##4 letters	THAT WITH HAVE THIS WILL YOUR FROM THEY KNOW WANT BEEN GOOD MUCH SOME TIME VERY WHEN COME HERE JUST LIKE LONG MAKE MANY MORE ONLY OVER SUCH TAKE THAN THEM WELL WERE
##5 letters	ABOUT WHERE WHICH THEIR THERE TODAY EVERY WOULD AFTER OTHER BEING FIRST GREAT THESE SINCE UNDER WHERE WHILE AFTER
##6+ letters	THROUGH PEOPLE BETWEEN BEFORE
##-ION	-TION -ATION -ITION
##-OUS	-IOUS -EOUS -ATIOUS -ITIOUS
##-IVE	-ATIVE -ITIVE
##Prefixes	DE- DIS- EN- EM- IN- IM- MIS- OVER- PRE- RE- UN-
##Suffixes	-ABLE -AL -ED -EN -ER -EST -FUL -IBLE -IC -ING -ION -IVE -LESS -LY -MENT -NESS -OUS
##H	CH SH TH PH WH
##K	CK SK LK KE
##Q	QU
##X	EX
##'T	WON'T DON'T ISN'T AREN'T WEREN'T SHOULDN'T DIDN'T CAN'T
##'S	HE'S SHE'S
##'D	I'D HE'D SHE'D THEY'D
##'M	I'M
##'RE	THEY'RE YOU'RE
##'VE	THEY'VE YOU'VE
##'LL	I'LL HE'LL SHE'LL THEY'LL IT'LL

the_dictionary = {"A" : "_", "B" : "_", "C" : "_", "D" : "_", "E" : "_", "F" : "_", "G" : "_", "H" : "_", "I" : "_",
                  "J" : "_", "K" : "_", "L" : "_", "M" : "_", "N" : "_", "O" : "_", "P" : "_", "Q" : "_", "R" : "_",
                  "S" : "_", "T" : "_", "U" : "_", "V" : "_", "W" : "_", "X" : "_", "Y" : "_", "Z" : "_" , "," : ",","\n":"\n",
                  ":" : ":", "." : ".", "'" : "'", "-" : "-", " " : " ", ";" : ";", "!" : "!", "?" : "?", "0" : "0","1" : "1","2" : "2","3" : "3","4" : "4","5" : "5","6" : "6","7" : "7","8" : "8","9" : "9","%" : "%",}

freq_dictionary = {"A" : 0, "B" : 0, "C" : 0, "D" : 0, "E" : 0, "F" : 0, "G" : 0, "H" : 0, "I" : 0,
                  "J" : 0, "K" : 0, "L" : 0, "M" : 0, "N" : 0, "O" : 0, "P" : 0, "Q" : 0, "R" : 0,
                  "S" : 0, "T" : 0, "U" : 0, "V" : 0, "W" : 0, "X" : 0, "Y" : 0, "Z" : 0 , "," : 0,
                  "." : 0, "'" : 0, "-" : 0, " " : 0, ";" : 0, ":" : 0, "\"" : 0, "-": 0}
letters = ["A" , "B" , "C" , "D" , "E" , "F" , "G" , "H" , "I" ,
                  "J" , "K" , "L" , "M" , "N" , "O" , "P" , "Q" , "R" ,
                  "S" , "T" , "U" , "V" , "W" , "X" , "Y" , "Z"  ]

two_letter_list = ["OF","TO", "IN", "IT", "IS", "IF", "BE", "AS", "AT", "SO", "WE", "HE", "BY",
                   "OR", "DO", "ME", "MY", "UP", "AN", "GO", "NO", "US", "AM", "ON"]
three_letter_list = ["THE", "AND", "FOR", "ARE", "BUT", "NOT", "YOU", "ALL","ANY", "CAN",
                     "HAD", "HER", "WAS", "ONE", "OUT", "OUR","DAY", "GET", "HAS", "HIM",
                     "HIS", "HOW", "MAN", "NEW","NOW", "OLD", "SEE", "TWO", "WAY", "WHO",
                     "BOY", "DID","ITS", "LET", "PUT", "SAY", "SHE", "TOO", "USE","OWN"]    
four_letter_list = ["THAT", "WITH", "HAVE", "THIS", "WILL", "YOUR", "GOAl", "FROM",
                    "THEY","KNOW", "WANT", "BEEN", "GOOD", "MUCH",
                    "SOME", "TIME", "LIFE","LIVE", "LIKE", "LOVE", "LONG", "ELSE"]
five_letter_list = ["ABOUT", "WHERE", "WHICH", "THEIR", "THERE", "TODAY", "EVERY", "HONEST", "WOULD", "AFTER", "OTHER", "BEING", "FIRST", "GREAT",
                    "THESE", "SINCE", "UNDER", "WHERE",
                    "WHILE", "THING", "THOSE", "OTHER", "GOALS"]
six_letter_list = ["BEFORE", "PEOPLE", "ACHIEVE", "SECOND", "ALWAYS", "THINGS", "OTHERS"]

double_letter_word_middle_list = ["WEEP", "SEEN", "SEEM", "SEED", "SEEK", "SEER", "SEEP", "SOON", "SOOT","ROOM", "ROOD", "ROOT", "REEL", "REEF", "REED",
                                  "NEED", "PEEL", "DOOR", "DOOM", "COON", "BEEN", "BEER", "BEET", "BEEP", "WEED", "WEEK",
                                  "POOL", "POOF", "POOR", "PEEK", "HOOP", "BOOM", "BOOT", "BOOK", "TEEN", "TEEM", "TEED", "TOOL",
                                  "HOOD", "HOOF", "HOOT", "JEEP", "KEEN", "KEEL", "KEEP", "FEEL", "FEET", "FOOT", "FOOD",
                                  "FOOL", "HEED", "HEEL", "NEED", "PEEL","PALL", "POOL", "POOF"]

double_letter_4word_end_list = ["CELL", "DELL", "DOLL", "FALL", "FELL" "POLL", "PASS", "ROLL", "SASS", "SELL","SILL", "TALL", "TELL", "WILL", "WALL", "WELL", "WATT", "HILL", "HULL", "LESS", "MALL","PALL"]
double_letter_3word_end_list = ["ALL", "ADD", "BEE", "BOO", "ELL", "EBB", "EGG", "FEE", "GOO", "TOO", "TEE", "SEE","ILL"]
contraction_list = ["WON'T", "DON'T", "I'VE", "ISN'T", "AREN'T", "WEREN'T", "SHOULDN'T", "DIDN'T", "CAN'T", "HE'S", "SHE'S",
                    "IT'S", "I'D", "HE'D", "SHE'D", "THEY'D", "I'M", "THEY'RE", "YOU'RE", "THEY'VE", "YOU'VE", "I'LL",
                    "HE'LL", "SHE'LL", "THEY'LL", "IT'LL", "WOULDN'T"]
triple_dipthongs = ["THE","AND", "THA", "ENT", "ION", "TIO", "FOR", "NDE", "HAS", "NCE", "EDT", "TIS", "OFT", "STH", "MEN"]

def unused_letters():
    letters = ["A" , "B" , "C" , "D" , "E" , "F" , "G" , "H" , "I" ,
                  "J" , "K" , "L" , "M" , "N" , "O" , "P" , "Q" , "R" ,
                  "S" , "T" , "U" , "V" , "W" , "X" , "Y" , "Z"  ]
    for key, value in the_dictionary.items():
        if (value in letters):
            letters.remove(value)
    print("Unused letters: ", letters)    

def shorten_dict(dicti):
    short_freq = {}
    for k in dicti.keys():
#        print(k)
        if dicti[k] > 1:
            short_freq[k] = dicti[k]
    print(short_freq)
#    print("short_freq()", sorted(short_freq.items(), key = lambda kv : kv[0], reverse = True))
#    print(short_freq)
    
def check_freq():
    for ch in the_code:
        if ch in freq_dictionary:
            freq_dictionary[ch] += 1
        else:
            freq_dictionary[ch] = 1
    print( {k: v for k, v in sorted(freq_dictionary.items(), key = lambda item: item[1], reverse = True)})
    print("E T A O I N S H R D L U")
def str_append_list_join(s,n):
    string_list = []
    i = 0
    while i < n:
        string_list.append(s)
def show_code_results():
    global the_code
    global the_dictionary
    results = []
##    print('show_code_results(): the_code ', the_code)
    for char in the_code:
        results.append(the_dictionary[char])
    results_string = ''.join(results)
    print(results_string)
    print(the_code, " quote number: ",quote_num)
    
    
def show_2_3_letter_results(d_p_dict):
#    print(d_p_dict)
    key_results = []
    for key in d_p_dict.keys():
        key_results.append(key)
    key_results_string = '  '.join(key_results)
    results = []
    for chars in key_results_string:
        results.append(the_dictionary[chars])
    results_string = ''.join(results)
    print()
    print(results_string)
    print(key_results_string)
    
def double_letter(code):
    print("replacing ", code)
    word_len = len(code)
    if word_len == 3:
        word_list = double_letter_3word_end_list
    elif word_len == 4:
        if code[1] == code[2]:
            word_list = double_letter_word_middle_list
        else:
            word_list = double_letter_4word_end_list
    else:
        print("error - word length")
        return
    for trial_word in word_list:
        for index in range(word_len):
            the_dictionary[code[index]] = trial_word[index]
        show_code_results()
        print("replaced ", code, "with ", trial_word)
        #okay = "Y" == input("Okay?  y or n o").upper()
        status = input("Okay?  y or n or q)uit").upper()
        if status == "Y":
            break
        elif status == "Q":
            for ch in code:
                the_dictionary[ch] = "_"
            show_code_results()
            break
        else:
            if index == word_len:
                for ch in code:
                    if ch != "'":
                        the_dictionary[ch] = "_"
                    
def contranctions(code):
    print("replacing ", code)
    word_len = len(code)
    for trial_word in contraction_list:
        print("trying ", trial_word)
        if len(trial_word) == word_len:
            for index in range(word_len):
                the_dictionary[code[index]] = trial_word[index]
            show_code_results()
            print("replaced ", code, "with ", trial_word)
        #okay = "Y" == input("Okay?  y or n o").upper()
            status = input("Okay?  y or n or q)uit").upper()
            if status == "Y":
                break
            elif status == "Q":
                for ch in code:
                    the_dictionary[ch] = "_"
                show_code_results()
                break
            else:
                if index == word_len:
                    for ch in code:
                        the_dictionary[ch] = "_"
                    break
    
    
quote_num = ""
answer = ""
if the_code == "":
    input_string = "Do you want to use " + temp_num + " as the quote number? ('y or n')"
    answer = input(input_string)
    answer = answer.upper()
    if answer != 'N':
        quote_num = temp_num
    else:
        quote_num = input("input the quote number ->  ")
    print('quote_num',quote_num)
    the_code = quote_reader.get_cryptogram(int(quote_num))
    ##YDGHOHZ NZCQV VDB ECV PYKIX KP KW, PYHZH KW C SMCNH TDZ GYCP VDB GCIP PD RD CIR GYD VDB GCIP PD AH - RCOKR ADGKH
the_code = the_code.upper()
print(the_code)
check_freq()

dipth_dict = {}

code = the_code.replace("'","zzzz")
table = str.maketrans(dict.fromkeys(string.punctuation))
stripped_code = code.translate(table)   # no punctuation in 'code' now but ' is "zzzz"
stripped_code = stripped_code.replace("zzzz","'")
for index in range(len(stripped_code) - 1):
    #print("dipth_dict", dipth_dict)
    dip = stripped_code[index] + stripped_code[index + 1]
    if dip in dipth_dict:
        dipth_dict[dip] += 1
    else:
        dipth_dict[dip] = 1    
#  dipth_dict sorting
dipth_dict = {k: v for k, v in sorted(dipth_dict.items(), key = lambda item: ( item[1]), reverse = True)}
##print("sorted --->>> ", dipth_dict)
##print(" TH ER ON AN RE HE IN ED ND HA AT EN ES")
##print("Dipthongs: ", dipth_dict)

lead_dict ={}
last_dict = {}
dip_dict = {}
for k in dipth_dict:
    if k[0] == " ":
        lead_dict[k] = dipth_dict[k]
#        #del dipth_dict[k]
    elif k[1] == " ":
        last_dict[k] = dipth_dict[k]
        #del dipth_dict[k]
    else:
        dip_dict[k] = dipth_dict[k]
lead_code_letter = " " + the_code[0]
last_code_letter = the_code[-1] + " "
if lead_code_letter in lead_dict:
    lead_dict[lead_code_letter] += 1
else:
    lead_dict[lead_code_letter] = 1
if last_code_letter in last_dict:
    last_dict[last_code_letter] += 1
else:
    last_dict[last_code_letter] = 1
    
def print_dipths():
    print("leading letters: ",shorten_dict(lead_dict), "  T O A W B C D")
    print("last letter: ", shorten_dict(last_dict), "  E S T D N R Y")
    print("dip_dict", shorten_dict )
    print("dip_dict", shorten_dict(dip_dict))
    print(" TH ER ON AN RE HE IN ED ND HA AT EN ES")
    
print_dipths()

trigraph_dict = {}
def print_trigraphs(trigraph_dict): #local and global trigraph_dict
    for index in range(len(the_code) - 2):
        tri = the_code[index] + the_code[index + 1] + the_code[index + 2]
        if " " not in tri:
            if tri in trigraph_dict:
                trigraph_dict[tri] += 1
            else:
                trigraph_dict[tri] = 1
   
    trigraph_dict =  {k: v for k, v in sorted(trigraph_dict.items(), key = lambda item: ( item[1]), reverse = True)}#{k: v, for k, v in sorted(trigraph_dict.items(), key = lambda item: item[1])}  #sorted(trigraph_dict.keys() #, key = lambda kv : (kv[1], kv[0]))
    print(trigraph_dict)
    if len(trigraph_dict) != 0:
        print("THE AND THA ENT ION TIO FOR NDE HAS NCE EDT TIS OFT STH MEN")

print_trigraphs(trigraph_dict)


def word_insert(code, real):
    for index in range(len(code)):
        print(index)
        the_dictionary[code[index]] = real[index]
        
word_to_replace = ""

def dip3(code):
    print("replacing ", code)
    for trial_letters in triple_dipthongs:
        for index in range(3):
            the_dictionary[code[index]] = trial_letters[index]
        show_code_results()
        print("replaced ", code, "with ", trial_letters)
        #okay = "Y" == input("Okay?  y or n o").upper()
        status = input("Okay?  y or n or q)uit").upper()
        if status == "Y":
            break
        elif status == "Q":
            for ch in code:
                the_dictionary[ch] = "_"
            show_code_results()
            break
        else:
            if index == word_len:
                for ch in code:
                    the_dictionary[ch] = "_"
                break
    for ch in code:
        the_dictionary[ch] = "_"
    show_code_results()
            
def check_list(code):
    global the_dictionary
    print("replacing ", code)
    word_len = len(code)
    if word_len == 2:
        word_list = two_letter_list
    elif word_len == 3:
        word_list = three_letter_list
    elif word_len == 4:
        word_list = four_letter_list
    elif word_len == 5:
        word_list = five_letter_list
    for trial_word in word_list:
        for index in range(word_len):
            the_dictionary[code[index]] = trial_word[index]
        show_code_results()
        print("replaced ", code, "with ", trial_word)
        #okay = "Y" == input("Okay?  y or n o").upper()
        status = input("Okay?  y or n or q)uit").upper()
        status = status.upper()
        if status == "Y":
            break
        elif status == "Q":
            for ch in code:
                the_dictionary[ch] = "_"
            show_code_results()
            break
        else:
            if index == word_len:
                for ch in code:
                    the_dictionary[ch] = "_"
                break
    for ch in code:
        the_dictionary[ch] = "_"
    show_code_results()
            
def check_pat_list(code, pat_list):
    print("replacing ", code, " using ", pat_list)
    word_len = len(code)
    for word in pat_list:
        t_word = word.upper()
        for index in range(word_len):
            the_dictionary[code[index]] = t_word[index]
        show_code_results()
        print("replaced ", code, "with ", t_word)
        #okay = "Y" == input("Okay?  y or n o").upper()
        status = input("Okay?  y or n or q)uit").upper()
        if status == "Y":
            break
        elif status == "Q":
            for ch in code:
                the_dictionary[ch] = "_"
            show_code_results()
            break
        else:
            if index == word_len:
                for ch in code:
                    the_dictionary[ch] = "_"
                break
                    
        
while True:
    print()
    mode = input("Changes?  N)ew key:value  D)elete key:value L)ist dictionary S)how results status A)lphabet  ->  ")
    mode = mode.upper()
    if mode != "":
        if mode[0] == "N":
            print("?") 
            if len(mode) > 2:
#        letters = input("code letter -> ")
                code_letter = mode[2].upper()
            #real_letter = input("real letter -> ")
                real_letter = mode[1].upper()
                the_dictionary[code_letter] = real_letter
            elif mode[0]:
                print("need 2 letters with this option")
            print()
            show_code_results()
        elif mode[0] == "C": # Clears all the letters
            for char in the_code:
                if char in letters:
                    the_dictionary[char] = "_"
            print()
            show_code_results()
        elif mode == "L":
        #check_freq()
            print(freq_dictionary)
        elif mode == "S":# Show all the code and letter found so far
            print()
            show_code_results()
        elif mode == "S+":
            print()
            show_code_results()
            show_2_3_letter_results(dip_dict)
            show_2_3_letter_results(trigraph_dict)
        elif mode[0] == "D":
            if len(mode) == 1:
                code_letter = input("code letter -> ")
                code_letter = code_letter.upper()
            else:
                code_letter = mode[1]
            the_dictionary[code_letter] = "_"
            print()
            show_code_results()
        elif mode == "23":
            print_dipths()
            print_trigraphs(trigraph_dict)
            print()
            show_code_results()
            print(" show_2_3_letter_results(dip_dict)")
            show_2_3_letter_results(dip_dict)
            show_2_3_letter_results(trigraph_dict)
        elif mode == "A":
            unused_letters()
        elif mode == "F":
            print("FREQ:", {k: v for k, v in sorted(freq_dictionary.items(), key = lambda item: item[1], reverse = True)})
            print("E T A O I N S H R D L U")
            print_dipths()
            print(trigraph_dict)
            if len(trigraph_dict) != 0:
                print("THE AND THA ENT ION TIO FOR NDE HAS NCE EDT TIS OFT STH MEN")
            unused_letters()
            print()
            show_code_results()
        elif mode == "D3":
            print("DIP3")
            code_letters = input("code letters => ")
            if len(code_word) != 3:
                print("error in format")
                break
            dip3(code_letters)
        elif mode == "W":
            code_word = input("code word => ")
            code_word = code_word.upper()
            word_to_replace = code_word
            real_word = input("real word => ")
            real_word = real_word.upper()
            if len(code_word) == len(real_word):
                word_insert(code_word, real_word)
                show_code_results()
            else:
                print("error - different word lengths ")
        elif mode == "WS":   # code word is the same
            code_word = word_to_replace
            print("replacing =>",code_word)
            real_word = input(" real word => ")
            real_word = real_word.upper()
            if len(code_word) == len(real_word):
                word_insert(code_word, real_word)
                show_code_results()
            else:
                print("error - different word lengths ")   
        elif mode == "LIST":
            code_word = input("code word => ")
            if code_word == "":
                print("error -  no code word")
                break
            code_word = code_word.upper()
            check_list(code_word)
        elif mode == "LISTPAT":
            code_word = input("code word => ")
            if code_word == "":
                print("error -  no code word")
                break
            code_word = code_word.upper()
            print('code_word ', code_word)
            str_words = input("Enter the words to test")
            list_words = []
            list_words = str_words.split("', '")
            print('str_words ', str_words, 'list_words ',list_words)
            check_pat_list(code_word, list_words)
        elif mode == "EE":
            code_word = input("code word => ")
            if code_word == "":
                print("error -  no code word")
                break
            code_word = code_word.upper()
            double_letter(code_word)
        elif mode == "'":
            code_word = input("code word => ")
            if code_word == "":
                print("error -  no code word")
                break
            code_word = code_word.upper()
            contranctions(code_word)
        elif mode == "PAT":  # for Find word Pattern
            crypto_word_finder_module.find_word_pattern()
        elif mode == "P_NAME":  # for Find name Pattern
            crypto_word_finder_module.find_name_pattern()
        else:
            print("???")
                
                



