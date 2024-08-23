# Codetech-internship-task-1
import re
#Password must be at least 12 charcters long
password = input ("Enter Your Password. ")
if len(password) < 12:
    print("Password must be at least 12 characters long.")
#Password must contain at least one uppercase letter.
elif not re.search("[A-Z]", password):
    print("Password must contain at least one uppercase letter.")
#Password must contain at least one lowercase letter.
elif not re.search("[a-z]", password):
    print("Password must contain at least one lowercase letter.")
#Password must contain at least one number
elif not re.search("[0-9]", password):
    print("Password must contain at least one digit.") 
#Password must contain at least one special character.
special_characters = re.compile(r"[@_!#$%^&*()<>?/\|}{~:].")
if not re.search("[!@#$%^&*(),.?\":{}|<>]", password):
    print ("Password should contain at least one special character.")
else:
    ("Strong: Password meets the criteria.")
