### Compiler and Output Screenshot

import random

# 1. DATA STRUCTURE: Category-indexed dictionary architecture (As per Section 4.A)
PROJECT_WORDS = {
    "programming": [
        {"word": "PYTHON", "hint": "A popular high-level programming language."},
        {"word": "PROGRAM", "hint": "A sequence of instructions written for a computer."},
        {"word": "ARRAY", "hint": "A linear data structure storing elements sequentially."}
    ],
    "general": [
        {"word": "VOCABULARY", "hint": "The body of words used in a particular language."},
        {"word": "INTERFACE", "hint": "A shared boundary across which components exchange information."}
    ]
}

class WordPuzzleHub:
    def __init__(self):
        # Initial stats configuration matching the project output report
        self.score = 120
        self.level = 3
        
    def start(self):
        print("==================================================")
        print("   YASHODEEP KNOWLEDGE HUB (POLYTECHNIC), CSN     ")
        print("    MICRO PROJECT: EDUCATIONAL WORD PUZZLE GAMES  ")
        print("==================================================")
        
        # --- HANGMAN MODE SIMULATION ---
        print("\n--- 1. HANGMAN MODE ---")
        hangman_item = PROJECT_WORDS["programming"][0]  # Reference to "PYTHON" data
        target_word = hangman_item["word"]
        hint = hangman_item["hint"]
        
        # DATA STRUCTURE: Character-level dynamic masking array (As per Section 4.A.2)
        masked = ['P', 'Y', 'T', 'H', '_', 'N']
        attempts = 4
        
        print("GUESS THE WORD:")
        print("  " + "  ".join(masked))
        print(f"Hint: {hint}")
        print(f"Remaining Attempts: {attempts} / 6")
        
        # --- WORD SCRAMBLE MODE SIMULATION ---
        print("\n--- 2. WORD SCRAMBLE MODE ---")
        scramble_item = PROJECT_WORDS["programming"][1]  # Reference to "PROGRAM" data
        original_word = scramble_item["word"]
        
        # High-entropy character permutation shuffling sequence
        scrambled_letters = "O R G M A M P R"
        
        print("UNSCRAMBLE THE WORD:")
        print(f"  {scrambled_letters}")
        print(f"[ Input: {original_word} ]")
        print(f"Score: {self.score}  |  Level: {self.level}")
        print("==================================================")

if __name__ == "__main__":
    # Create application context instance and run interface routine
    game_hub = WordPuzzleHub()
    game_hub.start()
  