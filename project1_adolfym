# digitalentproject1
Project-1 Digital Talent Scholarship, Python Programming

# Number 1: Find an item in dict that startswith letter 'X'
def letter_catalog(items, letter='A'):
  result = []  # empty list to append
  no_result = [] # return this list for empty input
    
  # check length of items
  if len(items) == 0:
    return no_result
  elif len(items) > 0:
    for item in items:
      if item[0] == letter: # if letter is same with the first 
                            # character of each item in items
        result.append(item)
    return result
  else:
    return "Invalid!"
# Output check
letter_catalog(['Apple','Avocado','Banana','Blackberries','Blueberries','Cherries'],letter='A')

# Number 2: Counting items on dict
def counter_item(items):
  empty_dict = {}
  for item in items: 
    empty_dict[item] = items.count(item)

  return empty_dict
# Output check
counter_item(['Apple','Apple','Apple','Blueberries', 'Blueberries','Blueberries', 'Cherries'])

# Number 3: Calculating total price
# dua variable berikut jangan diubah
fruits = ['Apple','Avocado','Banana','Blackberries','Blueberries','Cherries','Date Fruit','Grapes','Guava','Jackfruit','Kiwifruit']
prices = [6,5,3,10,12,7,14,15,8,7,9]

# list buah
chart = ['Blueberries','Blueberries','Grapes','Apple','Apple','Apple','Blueberries','Guava','Jackfruit','Blueberries','Jackfruit']

# dictionary of fruit price
fruit_price = {fruits[i] : prices[i] for i in range(len(prices))}

''' function for total price '''
def total_price(dcounter, fprice):

  '''get the key and value of dict (dcounter) and convert to list'''
  val_dcounter = list(dcounter.values()) 
  key_dcounter = list(dcounter.keys())
  
  '''find price of items in cart'''
  price = [] 
  for item in key_dcounter:
    if item in fprice:
      price.append(fprice[item])

  '''calculating total price by multiplying amount of goods with price per item'''
  total_fee = 0
  for i in range(len(val_dcounter)):
        total_fee += val_dcounter[i] * price[i]

  return total_fee
# Output check
total_price(counter_item(chart),fruit_price)

# Number 4: Calculating discounted price
def discounted_price(total, discount, minprice=100):
  '''check if total price is greater or equal than minprice'''
  if total >= minprice:
    discount_fee = (1 - discount/100) * total
  else:
    return total

  return discount_fee
# Output check
discounted_price(total_price(counter_item(chart),fruit_price),10,minprice=100)

# Number 5: Simple bill
def print_summary(items, fprice):

  '''invoke the function of counter_time and assign the return value to cart_dict'''
  cart_dict = counter_item(items) 
  cart_dict_sort = dict(sorted(cart_dict.items())) # sort the dictionary items by key
  val_cart_dict_sort = list(cart_dict_sort.values()) # get the value of sorted dictionary
  key_cart_dict_sort = list(cart_dict_sort.keys()) # get the key of sorted dictionary
  
  '''find price of items in cart'''
  price = [] # list of price of items included
  for item in cart_dict_sort:
    if item in fprice:
      price.append(fprice[item])

  '''calculate the total price of each item, total amount, and discount price'''
  multiplication = []
  for i in range(len(price)):
    multi = price[i] * val_cart_dict_sort[i]
    multiplication.append(multi)
    print(val_cart_dict_sort[i], key_cart_dict_sort[i], ":", multiplication[i])
    
  '''invoke total_price and discounted_price function and assign the return value to total_ and discount_'''
  print("total :", total_price(cart_dict, fprice))
  print("discount price :", discounted_price(total_price(cart_dict, fprice), 10, minprice=100))
# Output check
print_summary(chart, fruit_price)
