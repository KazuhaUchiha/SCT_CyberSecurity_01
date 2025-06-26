def caesar_encrypt(plaintext, shift):
    encrypted_text = ""
    for char in plaintext:
        if char.isalpha():  
            shift_base = ord('A') if char.isupper() else ord('a')
            # Shift the character and wrap around the alphabet
            encrypted_char = chr((ord(char) - shift_base + shift) % 26 + shift_base)
            encrypted_text += encrypted_char
        else:
            encrypted_text += char 
    return encrypted_text

def caesar_decrypt(ciphertext, shift):
    return caesar_encrypt(ciphertext, -shift) 

def main():
    while True:
        choice = input("Would you like to (E)ncrypt or (D)ecrypt? (Q to quit): ").strip().upper()
        if choice == 'Q':
            break
        elif choice in ['E', 'D']:
            text = input("Enter your text: ")
            shift = int(input("Enter the shift value (1-25): "))
            if choice == 'E':
                encrypted = caesar_encrypt(text, shift)
                print(f"Encrypted text: {encrypted}")
            else:
                decrypted = caesar_decrypt(text, shift)
                print(f"Decrypted text: {decrypted}")
        else:
            print("Invalid choice. Please choose E, D, or Q.")

if __name__ == "__main__":
    main()
