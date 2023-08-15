# Speed-Typing-Test-in-Python
import time

def typing_speed_test():
    text = "The quick brown fox jumps over the lazy dog"
    print("Type the following text:")
    print(text)
    input("Press Enter when you're ready to start...")
    
    start_time = time.time()
    user_input = input("Start typing: ")
    end_time = time.time()
    
    elapsed_time = end_time - start_time
    words = text.split()
    user_words = user_input.split()
    
    correct_words = 0
    for i in range(min(len(words), len(user_words))):
        if words[i] == user_words[i]:
            correct_words += 1
    
    accuracy = (correct_words / len(words)) * 100
    words_per_minute = (len(user_words) / elapsed_time) * 60
    
    print("\nTime taken:", round(elapsed_time, 2), "seconds")
    print("Accuracy:", round(accuracy, 2), "%")
    print("Words per minute:", round(words_per_minute))
    
typing_speed_test()
