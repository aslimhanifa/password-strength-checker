# Password Strength Checker
A Python tool to analyze password strength using regex and entropy calculation.

## Features
✅ Checks password complexity  
✅ Rates security level  
✅ Provides recommendations  

import re

def check_password_strength(password):
    strength = 0
    if len(password) >= 8:
        strength += 1
    if re.search(r'[A-Z]', password):
        strength += 1
    if re.search(r'[a-z]', password):
        strength += 1
    if re.search(r'\d', password):
        strength += 1
    if re.search(r'[!@#$%^&*(),.?":{}|<>]', password):
        strength += 1

    return strength

password = input("Enter your password: ")
strength = check_password_strength(password)

print(f"Password Strength: {strength}/5")




