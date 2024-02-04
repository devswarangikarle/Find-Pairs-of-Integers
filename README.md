# Find-Pairs-of-Integers
You are given two integers - n, m. Find the number of pairs (a, b) such that  a2 + b = n  a + b2 = m   Both a and b are greater than 0.

from math import isqrt

def find_pairs(n, m):
    count = 0

    for a in range(1, isqrt(n) + 1):
        b = n - a**2

        if b >= 1 and (m - b**2) == a:
            count += 1

    return count

# Input
n, m = map(int, input().split())

# Output
result = find_pairs(n, m)
print(result)

