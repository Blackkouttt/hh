# hh
hhhh
import os
from random import randint

# Simulate commits for 365 days
for i in range(1, 365):
    for j in range(0, randint(1, 10)):
        d = str(i) + ' days ago'
        with open('file.txt', 'a') as file:
            file.write(d + '\n')  # Add a newline for better readability
        os.system('git add .')
        os.system(f'git commit --date="{d}" -m "Commit for {d}"')

# Push changes to the main branch
os.system('git push -u origin main')

