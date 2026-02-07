# Caesar Cipher

A simple Python implementation of the Caesar cipher encryption algorithm.

## What is a Caesar Cipher?

The Caesar cipher is one of the simplest and oldest encryption techniques. It works by shifting each letter in the text by a fixed number of positions in the alphabet. For example, with a shift of 3, 'A' becomes 'D', 'B' becomes 'E', and so on.

## Features

- Encrypt text using any shift value from 1 to 25
- Decrypt encrypted text by reversing the shift
- Preserves letter case (uppercase remains uppercase, lowercase remains lowercase)
- Non-alphabetic characters remain unchanged

## Usage

### Encrypting Text

```python
encrypted = encrypt("Hello World", 13)
print(encrypted)  # Output: Uryyb Jbeyq
```

### Decrypting Text

```python
decrypted = decrypt("Uryyb Jbeyq", 13)
print(decrypted)  # Output: Hello World
```

### Using the Core Function

You can also use the `caesar()` function directly:

```python
# Encrypt
encrypted = caesar("Secret message", 5, encrypt=True)

# Decrypt
decrypted = caesar("Xjhwjy rjxxflj", 5, encrypt=False)
```

## Example

The script includes a demonstration that decrypts the message:

```python
encrypted_text = 'Pbhentr vf sbhaq va hayvxryl cynprf.'
decrypted_text = decrypt(encrypted_text, 13)
print(decrypted_text)  # Output: Courage is found in unlikely places.
```

## Parameters

- **text** (str): The text to encrypt or decrypt
- **shift** (int): The number of positions to shift (1-25)
- **encrypt** (bool): True for encryption, False for decryption (used in the `caesar()` function)

## Error Handling

The function validates input and returns error messages for:
- Non-integer shift values
- Shift values outside the range of 1-25

## How It Works

The cipher creates a translation table by:
1. Taking the standard alphabet
2. Rotating it by the specified shift amount
3. Mapping each original letter to its shifted equivalent
4. Applying the translation while preserving case
## Note

The ROT13 cipher (shift of 13) is a special case of the Caesar cipher where encryption and decryption use the same operation, since 13 is exactly half of the 26-letter alphabet.
