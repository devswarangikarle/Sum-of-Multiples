# Sum-of-Multiples

Emma is working on a number puzzle involving three integers: a, b, and k. Her goal is to find the sum of the first k natural numbers that are divisible by either a or b. Can you help Emma solve this puzzle?

Input
The first line of the input consists of three space-separated integers a, b, and k.

Constraints
1 ≤ a, b, k ≤ 100

def sum_of_multiples(a, b, k):
    count = 0
    total_sum = 0
    num = 1

    while count < k:
        if num % a == 0 or num % b == 0:
            total_sum += num
            count += 1
        num += 1

    return total_sum

# Input
a, b, k = map(int, input().split())

# Output the result
print(sum_of_multiples(a, b, k))
