import datetime
import os

# Function to load the saved name if it exists
def load_name():
    if os.path.exists("name.txt"):
        with open("name.txt", "r") as file:
            return file.read().strip()
    return None

# Function to save the name to a file
def save_name(name):
    with open("name.txt", "w") as file:
        file.write(name)

# Main chatbot function
def chatbot():
    # Load the stored name if it exists
    name = load_name()

    while True:
        if not name:
            # Ask for the user's name if not remembered
            name = input("Hello! What's your name? ")
            save_name(name)
        
        # Print the current date and time
        now = datetime.datetime.now()
        print(f"Hello {name}! The current date and time is: {now.strftime('%Y-%m-%d %H:%M:%S')}")

        # Ask for email ID
        email = input("What's your email ID? ")

        # Check if user wants to exit the chatbot
        shutdown = input("Type 'shutdown' to exit or press Enter to continue: ").lower()
        if shutdown == "shutdown":
            print("Goodbye!")
            break

# Run the chatbot
if __name__ == "__main__":
    chatbot()
