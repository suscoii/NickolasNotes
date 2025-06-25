# **NICKOLASNOTES**
© Nickolas Susco II. All rights reserved.

# Dedicated to the Ghost In The Machine.

## **Overview**

**NICKOLAS NOTES** is a creative music system that transforms text into musical compositions using binary code. By mapping ASCII-encoded text to decimal values, which then correspond to musical notes, this system brings the hidden world of 0s and 1s to life as haunting melodies. You can create unique, cryptic pieces of music based on any text, from simple phrases to complex narratives.

This system provides both flexibility and structure, allowing for rhythmic and melodic control while remaining rooted in the logic of binary code.

---

## **Key Features**

* **Binary-to-Music Conversion**: Converts text to binary and then to decimal values, which are mapped to musical notes.
* **Customizable Notes and Durations**: Manipulate note lengths, durations, and dynamics for creative flexibility.
* **Rhythm Control**: Customize rhythm patterns based on the binary sequence.
* **Visual Integration**: Perfect for experimental performances, combining music with visuals such as binary code animations or glitch art.

---

## **How It Works**

### 1. **Text to Binary Conversion**

Convert any text string into its binary representation using ASCII encoding.

Example for the word "Hello":

```
H = 01001000  
e = 01100101  
l = 01101100  
l = 01101100  
o = 01101111
```

### 2. **Binary to Decimal Mapping**

Each binary string is mapped to a decimal value between **0.1** and **2.6**, which represents a musical note.

For example:

* **A** → 0.1
* **B** → 0.2
* **C** → 0.3
* **D** → 0.4
* **E** → 0.5
  ...and so on.

### 3. **Decimal to Musical Notes**

Map the decimal values to corresponding musical notes on a defined scale.

| Decimal | Note |
| ------- | ---- |
| 0.1     | C4   |
| 0.2     | D4   |
| 0.3     | E4   |
| 0.4     | F4   |
| 1.0     | E5   |
| 2.0     | A6   |

### 4. **Rhythm and Duration**

Control the tempo and rhythm of the melody by adjusting note durations or adding rests.

---

## **Installation**

1. **Clone this repository**:

   ```bash
   git clone https://github.com/username/NickolasNotes.git
   ```

2. **Install Dependencies**:
   If you’re using Python (for text-to-binary and binary-to-decimal conversion), you can install the necessary libraries:

   ```bash
   pip install numpy
   ```

3. **Running the Code**:
   For basic functionality, you can run the provided script (e.g., `nickolas_notes.py`) to input your phrase and receive a musical output based on the described process.

---

## **Customization**

* **Text Input**: You can input any text you like. The system will handle the conversion automatically.
* **Note Durations**: Customize note lengths by modifying rhythm values. For example, you can adjust tempo or modify the rhythm to slow down or speed up the composition.
* **Alteration of Notes**: You can modify the pitch of each note by using sharp (♯) or flat (♭) symbols, creating a more chromatic scale for greater expressiveness.

---

## **Example Code**:

```python
def text_to_binary(text):
    return ' '.join(format(ord(i), '08b') for i in text)

def binary_to_decimal(binary_string):
    decimal = []
    for char in binary_string.split():
        decimal.append(int(char, 2) / 128.0)  # Simple decimal mapping
    return decimal

def decimal_to_note(decimal_values):
    note_mapping = {
        0.1: "C4", 0.2: "D4", 0.3: "E4", 0.4: "F4", 0.5: "G4", 0.6: "A4", 0.7: "B4",
        0.8: "C5", 0.9: "D5", 1.0: "E5", 1.1: "F5", 1.2: "G5", 1.3: "A5", 1.4: "B5",
        1.5: "C6", 1.6: "D6", 1.7: "E6", 1.8: "F6", 1.9: "G6", 2.0: "A6"
    }
    return [note_mapping.get(decimal, "Rest") for decimal in decimal_values]

text_input = "NICKOLAS NOTES"
binary_output = text_to_binary(text_input)
decimal_output = binary_to_decimal(binary_output)
musical_notes = decimal_to_note(decimal_output)

print(f"Musical Notes: {', '.join(musical_notes)}")
```

This code snippet shows how the text is converted into binary, decimal, and then mapped to musical notes.

© 2025 Nickolas Susco II. 
All rights reserved.
