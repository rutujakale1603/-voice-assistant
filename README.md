# -voice-assistant
major project in python.

This Python script is designed to create a basic voice assistant named "Peter" using the pyttsx3 library for text-to-speech conversion and the speech_recognition library for speech recognition. Here's a breakdown of the code:

1. **Importing Libraries**: The script imports necessary libraries such as pyttsx3 for text-to-speech conversion, speech_recognition for speech recognition, webbrowser for opening web browsers, datetime for handling date and time, pyjokes for fetching jokes, and time for pausing execution.

2. **`sptext()` Function**: This function is responsible for capturing speech input from the microphone. It initializes a Recognizer instance, adjusts for ambient noise, listens for audio input, and attempts to recognize the speech using Google's speech recognition service. If successful, it prints the recognized speech and returns it.

3. **`speechtx(x)` Function**: This function is used to convert text to speech. It initializes a pyttsx3 engine, sets the voice and rate properties, says the input text, and waits for the speech to finish.

4. **Main Execution Block (`if __name__ == '__main__':`)**: 
   - It checks if the trigger phrase "hey peter" is present in the speech input obtained from `sptext()`. If found, it enters a loop to continuously listen for commands.
   - Inside the loop, it listens for commands using `sptext()`, converts them to lowercase, and checks for specific phrases like "your name", "how old are you?", "now time", "youtube", "jokes", and "exit".
   - If a specific command is recognized, it performs the corresponding action:
     - It responds with Peter's name if asked about its name.
     - It responds with its age if asked about its age.
     - It tells the current time if asked for the time.
     - It opens the YouTube website if the command contains "youtube".
     - It fetches and speaks a joke if the command contains "jokes".
     - It says "thank you" and exits if the command contains "exit".
   - The loop continues until the "exit" command is given.

5. **Else Block**: If the trigger phrase is not recognized in the initial speech input, it prints "thanks".

This code serves as a basic framework for a voice assistant that can perform simple tasks based on voice commands. You could further enhance it by adding more functionalities and improving the robustness of speech recognition and text-to-speech conversion.
