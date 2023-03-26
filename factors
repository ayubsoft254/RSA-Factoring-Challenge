import sys

def factorize(n):
    """
    Given a natural number n, return a list of all possible factorizations
    of n as a product of two smaller numbers.
    """
    factors = []
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            factors.append((i, n // i))
    return factors

# Check that the correct command line arguments were passed
if len(sys.argv) != 2:
    print("Usage: factors <file>")
    sys.exit(1)

# Open the input file and read the numbers one by one
with open(sys.argv[1]) as f:
    for line in f:
        n = int(line.strip())
        for factorization in factorize(n):
            print(f"{n}={factorization[0]}*{factorization[1]}")

