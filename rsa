import sys

def is_prime(n):
    """
    Check if a given number n is prime.
    """
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Check that the correct command line arguments were passed
if len(sys.argv) != 2:
    print("Usage: factor_primes <number>")
    sys.exit(1)

# Convert the input argument to an integer
n = int(sys.argv[1])

# Find the prime factors of the number
factors = []
for i in range(2, int(n**0.5) + 1):
    if n % i == 0 and is_prime(i) and is_prime(n // i):
        factors.append(i)
        factors.append(n // i)
        break

# Print the prime factors
if len(factors) == 2:
    print(f"{n}={factors[0]}*{factors[1]}")
else:
    print(f"{n} is a prime number")

