# Difference-between-two-lists-in-python

# Apporach-1
li1 = [10, 15, 20, 25, 30, 35, 40]
li2 = [25, 40, 35]

temp3 = []
for element in li1:
	if element not in li2:
		temp3.append(element)

print(temp3)

# Apporach-2
# Using list  comprehension
li1 = [10, 15, 20, 25, 30, 35, 40]
li2 = [25, 40, 35]

s = set(li2)
temp3 = [x for x in li1 if x not in s]
print(temp3)

# Apporach-3

# Use Numpy to Compare Two Lists in Python
import numpy as np
li1 = np.array([10, 15, 20, 25, 30, 35, 40])
li2 = np.array([25, 40, 35])

dif1 = np.setdiff1d(li1, li2)
dif2 = np.setdiff1d(li2, li1)

temp3 = np.concatenate((dif1, dif2))
print(list(temp3))

