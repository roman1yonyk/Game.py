import random

def початок():
    print("Ласкаво просимо у світ магії!")
    print("Ви - молодий маг, який вирушає у подорож за допомогою вивчення чарів та зустрічі із загадковими істотами.")
    print("Ваші дії впливають на весь світ. Оберіть свій шлях мудро.")

def вибір_дії():
    print("\nОберіть вашу наступну дію:")
    print("1. Вивчити нове закляття")
    print("2. Подолати монстра")
    print("3. Розмовитися з ворожкою")
    вибір = input("Ваш вибір: ")
    return вибір

def вивчити_закляття():
    закляття = random.choice(["Вогненний кулак", "Лікування ран", "Магічний щит", "Тіньова стріла"])
    print(f"Ви вивчили нове закляття: {закляття}!")

def подолати_монстра():
    успіх = random.choice([True, False])
    if успіх:
        print("Вітаємо! Ви перемогли монстра та здобули скарби.")
    else:
        print("Ви не змогли подолати монстра. Спробуйте ще раз.")

def розмовитися_з_ворожкою():
    print("Ворожка розкрила перед вами таємницю магії і надала вам мудрі поради.")

початок()

while True:
    дія = вибір_дії()

    if дія == "1":
        вивчити_закляття()
    elif дія == "2":
        подолати_монстра()
    elif дія == "3":
        розмовитися_з_ворожкою()
    else:
        print("Невірний вибір. Спробуйте ще раз.")

    продовжити = input("Бажаєте продовжити гру? (так/ні): ")
    if продовжити.lower() != "так":
        print("Дякуємо за гру! До побачення!")
        break
