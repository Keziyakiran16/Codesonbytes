# Codesonbytes
import random
n=int(input("Enter number of questions you want to ask:"))

# Define a list of 30 questions and their corresponding answers
questions = [
    {"question": "What is the capital of India?", "answer": "New Delhi"},
    {"question": "Which planet is known as the Red Planet?", "answer": "Mars"},
    {"question": "What is the largest mammal in the world?", "answer": "Blue whale"},
    {"question": "what is the capital of France?", "answer": "Paris"},
    {"question": "Who is the youngest one in the world?", "answer": "taehyung"},
    {"question": "Who wrote the play Romeo and Juliet?", "answer": "william Shakespeare"},
    {"question": "What is the largest planet in our solar system?", "answer": "Jupiter"},
    {"question": "what is the tallest mountain in the world?", "answer": "Mount Everest"},
    {"question": "Who is the known as father of modern physics?", "answer": "Albert Einstein"},
    {"question": "Who is the author to kill a mockingbird?", "answer": "Harper Lee"},
    {"question": "What is the primary function of the Heart?", "answer": "pumping blood throughout the Body"},
    {"question": "Who is the first president of United States?", "answer": "George Washington"},
    {"question": "What gas do plants absorb from the atmosphere?", "answer": "carbondioxide"},
    {"question": "what is the largest mammal on Earth?", "answer": "Blue Whale"},
    {"question": "what is the chemical symbol of Water?", "answer": "h2O"},
    {"question": "Who painted the Mona Lisa?", "answer": "Leonardo da Vinci"},
    {"question": "What is the captial of Australia?", "answer": "Canberra"},
    {"question": "What is the chemical symbol for carbon?", "answer": "C"},
    {"question": "What is the chemical symbol for Iron?", "answer": "Fe"},
    {"question": "What is the chemical symbol for silver?", "answer": "Ag"},
    {"question": "Who wrote war and peace?", "answer": "Leo Tolstoy"},
    {"question": "What is the currency of Brazil ?", "answer": "Brazillian Real"},
    {"question": "What is the youngest river in south america?", "answer": "Amazon river"},
    {"question": "What is the smallest planet in our solar system?", "answer": "Mercury"},
    {"question": "What is the freezing point of water in Celsius?", "answer": "0 degrees Celsius"},
    {"question": "Who painted the Starry Night?", "answer": "Vincent van Gogh"},
    {"question": "What is the currency of China?", "answer": "Chinese Yuan"},
    {"question": "What is the process by which plants convert sunlight into energy?", "answer": "Photosynthesis"},
    {"question": "What is the tallest mountain in North America?", "answer": "Denali"},
    {"question": " Who was the first person to walk on the moon?", "answer": "Neil Armstrong"},
]

def select_random_question(questions):
    """Select a random question from the list."""
    return random.choice(questions)

def main():
    score = 0
    num_questions = 5  # Change this to the number of questions you want to ask

    print("Welcome to the Quiz Game!")
    print("Please type your answers. Capitalization doesn't matter.\n")

    for _ in range(num_questions):
        question_data = select_random_question(questions)
        question = question_data["question"]
        correct_answer = question_data["answer"]

        print(question)
        user_answer = input("Your answer: ")

        if user_answer.lower() == correct_answer.lower():
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong. The correct answer is: {correct_answer}\n")

    print(f"You answered {score} out of {num_questions} questions correctly. Thanks for playing!")

if __name__ == "__main__":
    main()
