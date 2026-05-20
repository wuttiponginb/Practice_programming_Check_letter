import string

alphabet = string.ascii_letters
uppercase = string.ascii_uppercase
lowercase = string.ascii_lowercase
digits = string.digits
punctuation = string.punctuation


letter = str(input("Enter a message: "))
find_alphabet = 0
find_upper = 0
find_lower = 0
find_digit = 0
find_symbols = 0
find_swap_letter = " "
for i in letter:
    if i in alphabet[:]:
        find_alphabet += 1
        if i in uppercase[:]:
            find_upper += 1
        else:
            find_lower += 1
    elif i in digits[:]:
        find_digit += 1
    else:
        find_symbols += 1
print("Total alphabet = %s" % find_alphabet)
print("Total uppercase = %s" % find_upper)
print("Total lowercase = %s" % find_lower)
print("Total digits = %s" % find_digit)
print("Total symbols = %s" % find_symbols)

for x in letter:
    if x.islower():
        x = x.upper()
        find_swap_letter += x
    elif x.isupper():
        x = x.lower()
        find_swap_letter += x
    else:
        find_swap_letter += x
print("Swapped is %s"% find_swap_letter)
