import random
count=0
name =str(input ('User,Please enter your name :'))
print('\nProgram will randomly generate a number in the range you will give. ')
print(name,', Please try to guess the number ')
#Getting limits from the user
ll=int(input('\nPlease enter a lower limit: '))
ul=int(input('Please enter an upper limit: '))

a=random.randint(ll,ul)

#User can score points if he/she guesses correctly and here is the points system
  #first attempt - 100 points
  #second attempt - 75 points
  #Third attempt - 50 points
  #Fourth attempt - 25 points
  #Fifth attempt - 10 points
  #More than five attempts - 5 points

b= int(input('\nWhat do you think program number is ?\n')) #Making user to guess the number


while True:
  if (a>b):
    print('Program number is higher than ',b)
    count=count+1
    b=int(input(''))
  elif (a<b):
    print('Program number is lesser than ',b)
    count=count+1
    b=int(input(''))
  elif (a==b):
    count=count+1
    print('\nHurray! You got it and the number is ',b)
    break
  else:
    print('Invalid,Please enter again')
    b=int(input (''))

#getting the number of attempt user took to guess
if count==1:
  print('Congratulations, You did it in First attempt')
  print('You got 100 points')
elif count==2:
  print('Congratulations, You did it in Second attempt')
  print('You got 75 points')
elif count==3:
  print('Congratulations, You did it in Third attempt')
  print('You got 50 points')
elif count==4:
  print('Congratulations, You did it in Fourth attempt')
  print('You got 25 points')
elif count==5:
  print('Congratulations, You did it in Fifth attempt')
  print('You got 10 points')
else:
  print('Congratulations, But you took more than five attempts')
  print('You got 5 points')
