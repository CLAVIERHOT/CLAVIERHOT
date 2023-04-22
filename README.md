import random
import time

words = ['christo', 'princesse', 'camilla','batistepd', 'martinique', 'blanche','julien']


def main():
    print("CLAVIER EN FEU")
    print("Le but du jeu est de taper les mots qui apparaissent à l'écran aussi rapidement que possible.")
    input("Appuie sur ta touche entrer ou tu es un pd comme batiste euu.. je voulais dire tu es pas attirer par les femmes")

    correct_words = 0
    incorrect_words = 0
    start_time = time.time()

    while correct_words < 10:
        word = random.choice(words)
        print(f"\nTapez le mot suivant: {word}")
        user_input = input("> ")
        if user_input == word:
            correct_words += 1
            print("Bravo! Vous avez tapé le mot correctement.")
        else:
            incorrect_words += 1
            print(f"Désolé, le mot était {word}.")

    end_time = time.time()
    total_time = end_time - start_time
    accuracy = round((correct_words / (correct_words + incorrect_words)) * 100)
    print(f"Vous avez terminé en {total_time:.2f} secondes avec une précision de {accuracy}%.")
    print("bientot de retour en martnique hehe")

if __name__ == '__main__':
    main()
