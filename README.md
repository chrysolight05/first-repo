# first-repo
first repository on Github

import sys

def greet_user(name: str) -> str:
    """Generates a personalized greeting message."""
    if not name.strip():
        raise ValueError("Name cannot be empty!")
    return f"Hello, {name}! Welcome to my GitHub repository."

def main():
    print("--- GitHub Demo App ---")
    try:
        # Takes input from the terminal or defaults to 'Guest'
        user_name = sys.argv[1] if len(sys.argv) > 1 else input("Enter your name: ")
        message = greet_user(user_name)
        print(message)
    except ValueError as e:
        print(f"Error: {e}")
    except KeyboardInterrupt:
        print("\nGoodbye!")

if __name__ == "__main__":
    main()
