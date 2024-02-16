# Python-quiz-game
This is the basic outline to implement a simple quiz game using python codings
i used three questions within the code to implement this game


class Quiz:
    def __init__(self, questions):
        self.questions = questions
        self.score = 0
    def display_question(self, question):
        print(question)
    def display_result(self):
        print(f"Your final score is: {self.score}/{len(self.questions)}")
    def run_quiz(self):
        for question, answer in self.questions.items():
            self.display_question(question)
            user_answer = input("Your answer: ")
            if user_answer.lower() == answer.lower():
                print("Correct!")
                self.score += 1
            else:
                print("Incorrect.")
        self.display_result()
quiz_data = {
    "What is the capital of France?": "Paris",
    "What is 100 + 200": "300",
    "Who painted the Mona Lisa?": "Leonardo da Vinci"
}
quiz = Quiz(quiz_data)
quiz.run_quiz()
