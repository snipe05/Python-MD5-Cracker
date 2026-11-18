import hashlib
import sys

def crack_md5(target_hash, wordlist_file):
    with open(wordlist_file, 'r', encoding='latin-1') as f:
        for line in f:
            word = line.strip()
            hashed_word = hashlib.md5(word.encode()).hexdigest()
            if hashed_word == target_hash:
                print(f"Match found: {word}")
                return
    print("No match found.")

if __name__ == "__main__":
    if len(sys.argv) == 3:
        crack_md5(sys.argv[1], sys.argv[2])
    else:
        print("Usage: python3 cracker.py <hash> <wordlist>")
