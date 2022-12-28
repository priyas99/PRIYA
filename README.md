# taking the input from the user
# if the input is not a number then the program will ask for the input again
while True:
    try:
        N = int(input("Enter the value of N: "))
        break
    except ValueError:
        print("Please enter a number")
# defining a function to check if the cake can be cut into N equal pieces
def equal(N):
    if N%2==0:
        return True
    else:
        return False
# defining a function to check if the cake can be cut into N pieces of any size
def anysize(N):
    if N%2==0 or N%2==1:
        return True
    else:
        return False
# defining a function to check if the cake can be cut into N pieces such that no two of them are equal
def nonequal(N):
    if N%2==1:
        return True
    else:
        return False
# printing the result
print("The cake can be cut into",N,"equal pieces:",equal(N))
print("The cake can be cut into",N,"pieces of any size:",anysize(N))
print("The cake can be cut into",N,"pieces such that no two of them are equal:",nonequal(N))

