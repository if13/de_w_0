from collections import defaultdict
from collections import OrderedDict

purchases = [
    {"item": "apple", "category": "fruit", "price": 1.2, "quantity": 10},
    {"item": "banana", "category": "fruit", "price": 0.5, "quantity": 5},
    {"item": "milk", "category": "dairy", "price": 1.5, "quantity": 2},
    {"item": "bread", "category": "bakery", "price": 2.0, "quantity": 3},
]
#  list of dict

def total_revenue(purchases):
        return sum([p['price'] * p['quantity']  for p in purchases ])


def items_by_category(purchases):
    categories = defaultdict(list)
    for p in purchases:
        categories[p['category']].append(p['item'])

    return dict(categories)


def expensive_purchases(purchases, min_price):
    return [p for p in purchases if p['price'] * p['quantity']>=min_price]


def average_price_by_category(purchases):
    prices_in_category = defaultdict(list)
    for p in purchases:
        prices_in_category[p['category']].append(p['price'])

    return {k:sum(v)/len(v) for k,v  in prices_in_category.items()}


def most_frequent_category(purchases):
    count_in_category = defaultdict(int)
    for p in purchases:
        count_in_category[p['category']] += p['quantity']

    return sorted(OrderedDict(count_in_category), key= lambda x: x[1])[-1]

# Выводим результаты
print('Общая выручка:', total_revenue(purchases))
print('Товары по категориям:', items_by_category(purchases))
print('Покупки дороже 1.0:', expensive_purchases(purchases, 1))
print('Средняя цена по категориям:', average_price_by_category(purchases))
print('Категория с наибольшим количеством проданных товаров:', most_frequent_category(purchases))
