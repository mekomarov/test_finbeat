from telebot import TeleBot, types
from telebot.types import ReplyKeyboardMarkup, KeyboardButton, InlineKeyboardButton, InlineKeyboardMarkup


bot = TeleBot(TOKEN)

# Переменные с названиями различных типов занятий
var_pairClasses = 'Парные взрослые групповые занятия'
var_adultGroup = 'Взрослые групповые занятия'
var_kidsGroup = 'Детские групповые занятия'
var_person = 'Персональные занятия'
var_back = 'Назад'
var_novice = 'Новичек'
var_amateur = 'Любитель'
var_dancer = 'Танцор'
var_master = 'Мастер'
user_states = {}

# Абонементы для взрослых парных занятий
ticket_amateur_pairClasses = (
    'Вы выбрали\nАбонемент: Любитель\nЗанятий: 12\nСтоимость: 12240р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_novice_pairClasses = (
    'Вы выбрали\nАбонемент: Новичек\nЗанятий: 8\nСтоимость: 8800р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_dancer_pairClasses = (
    'Вы выбрали\nАбонемент: Танцор\nЗанятий: 16\nСтоимость: 15680р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_master_pairClasses = (
    'Вы выбрали\nАбонемент: Мастер\nЗанятий: 24\nСтоимость: 24192р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)

# Абонементы для взрослых групповых занятий
ticket_amateur_adultGroup = (
    'Вы выбрали\nАбонемент: Любитель\nЗанятий: 8\nСтоимость: 4800р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_novice_adultGroup = (
    'Вы выбрали\nАбонемент: Новичек\nЗанятий: 4\nСтоимость: 2900р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_dancer_adultGroup = (
    'Вы выбрали\nАбонемент: Танцор\nЗанятий : 12\nСтоимость: 6840р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_master_adultGroup = (
    'Вы выбрали\nАбонемент: Мастер\nЗанятий: 24\nСтоимость: 13440р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)

# Абонементы для детских занятий
ticket_amateur_kids = (
    'Вы выбрали\nАбонемент: Любитель\nЗанятий: 12\nСтоимость: 6600р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_novice_kids = (
    'Вы выбрали\nАбонемент: Новичек\nЗанятий: 8\nСтоимость: 4560р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_dancer_kids = (
    'Вы выбрали\nАбонемент: Танцор\nЗанятий: 16\nСтоимость: 8480р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)
ticket_master_kids = (
    'Вы выбрали\nАбонемент: Мастер\nЗанятий: 24\nСтоимость: 12960р\n'
    'Срок действия абонемента 4 недели.\n(с первого дня посещения занятия!)\nВходят ЛЮБЫЕ направления'
)

# Основное меню
def main_menu():
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
    buttons = [
        types.KeyboardButton(var_pairClasses),
        types.KeyboardButton(var_adultGroup),
        types.KeyboardButton(var_kidsGroup),
        types.KeyboardButton(var_person)
    ]
    for button in buttons:
        markup.add(button)
    return markup

#Оплата
def payment():
    markup = types.InlineKeyboardMarkup()
    buttons = [
        types.InlineKeyboardButton('Оплатить 💃',callback_data='ссылка')
    ]
    for button in buttons:
        markup.add(button)
    return markup

#Сайт
def site():
    markup = types.InlineKeyboardMarkup()
    buttons = [
        types.InlineKeyboardButton('Наш сайт ❤️',url='https://2dance-academy.ru/')
    ]
    for button in buttons:
        markup.add(button)
    return markup

# Подменю выбора абонемента для парных занятий
def level_pair_menu():
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
    levels = [
        types.KeyboardButton(var_novice),
        types.KeyboardButton(var_amateur),
        types.KeyboardButton(var_dancer),
        types.KeyboardButton(var_master),
        types.KeyboardButton(var_back)
    ]
    for level in levels:
        markup.add(level)
    return markup

# Подменю выбора взрослых групповых занятий
def level_adult_menu():
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
    levels = [
        types.KeyboardButton(var_novice),
        types.KeyboardButton(var_amateur),
        types.KeyboardButton(var_dancer),
        types.KeyboardButton(var_master),
        types.KeyboardButton(var_back)
    ]
    for level in levels:
        markup.add(level)
    return markup

# Подменю выбора абонемента для детских занятий
def level_kids_menu():
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
    levels = [
        types.KeyboardButton(var_amateur),
        types.KeyboardButton(var_novice),
        types.KeyboardButton(var_dancer),
        types.KeyboardButton(var_master),
        types.KeyboardButton(var_back)
    ]
    for level in levels:
        markup.add(level)
    return markup

# Команда старта
@bot.message_handler(commands=['start'])
def start_command(message):
    bot.send_message(message.chat.id, f"Добро пожаловать в 2dance {message.from_user.first_name}\nВся информация в нашем меню 👇")


# Команда сайт
@bot.message_handler(commands=['site'])
def start_command(message):
    bot.send_message(message.chat.id, 'На нашем сайте еще больше информации ', reply_markup=site())

#Команда абонемент
@bot.message_handler(commands=['subs'])
def start_command(message):
    bot.send_message(message.chat.id, 'Выбери абонемент', reply_markup=main_menu())


# Выбор категории занятий
@bot.message_handler(func=lambda message: message.text in [var_pairClasses, var_adultGroup, var_kidsGroup, var_person])
def category_choice(message):
    chat_id = message.chat.id
    user_states[chat_id] = message.text  # Сохраняем текущее состояние пользователя
    if message.text == var_pairClasses:
        bot.send_message(message.chat.id, "Выберите подходящий уровень:", reply_markup=level_pair_menu())
    elif message.text == var_kidsGroup:
        bot.send_message(message.chat.id, "Выберите подходящий уровень:", reply_markup=level_kids_menu())
    elif message.text == var_adultGroup:
        bot.send_message(message.chat.id, "Выберите подходящий уровень:", reply_markup=level_kids_menu())
    else:
        bot.send_message(message.chat.id, "Поддержка данной опции временно приостановлена.")


# Обработчик возвратов назад
@bot.message_handler(func=lambda message: message.text == var_back)
def go_to_main_menu(message):
    bot.send_message(message.chat.id, "Вернулись в главное меню", reply_markup=main_menu())

# Обработчик выбора абонемента
@bot.message_handler(func=lambda message: message.text in ["Любитель", "Новичек", "Танцор", "Мастер"])
def select_ticket_type(message):
    chat_id = message.chat.id
    current_category = user_states.get(chat_id)

    # Определяем текущий вид занятий
    if not current_category:
        bot.send_message(chat_id, "Что-то пошло не так. Попробуйте снова выбрать категорию занятий.")
        return

    user_text = message.text.lower()
    if current_category == var_pairClasses:
        tickets = {
            "любитель": ticket_amateur_pairClasses,
            "новичек": ticket_novice_pairClasses,
            "танцор": ticket_dancer_pairClasses,
            "мастер": ticket_master_pairClasses
        }
    elif current_category == var_kidsGroup:
        tickets = {
            "любитель": ticket_amateur_kids,
            "новичек": ticket_novice_kids,
            "танцор": ticket_dancer_kids,
            "мастер": ticket_master_kids
        }
    elif current_category == var_adultGroup:
        tickets = {
            "любитель": ticket_amateur_adultGroup,
            "новичек": ticket_novice_adultGroup,
            "танцор": ticket_dancer_adultGroup,
            "мастер": ticket_master_adultGroup
        }
    response = tickets.get(user_text)
    if response:
        bot.send_message(message.chat.id, response, reply_markup = payment())


# Запускаем бесконечный цикл приема сообщений
#bot.infinity_polling()
