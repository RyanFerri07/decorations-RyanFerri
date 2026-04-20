#decorations.py
# name: Ryan Ferri
# date: April 20, 2026
# description: determines decorations based on input

# Get input
user_input = input("enter a date(Mon Day): ")

# split input
pieces = user_input.split()

# check if the input is valid
if len(pieces) != 2:
    print("Error: Give a Valid Input(Mon Day)")
else:
    month = pieces[0]

# Check if Day is a number
    if not pieces[1].isdigit():
        print("Error: Give a Vaild Input(Mon Day)")
    else:
        day = int(pieces[1])

    # convert months to numbers
        if month == "Jan":
            month_num = 1
        elif month == "Feb":
            month_num = 2
        elif month == "Mar":
            month_num = 3
        elif month == "Apr":
             month_num = 4
        elif month == "May":
            month_num = 5
        elif month == "Jun":
            month_num = 6
        elif month == "Jul":
            month_num = 7
        elif month == "Aug":
            month_num = 8
        elif month == "Sep":
           month_num = 9
        elif month == "Oct":
            month_num = 10
        elif month == "Nov":
            month_num = 11
        elif month == "Dec":
            month_num = 12
        else:
            print("Error: Give a Valid Input(Mon Day)")
            month_num = -1

#convert date to comparable number
        if month_num != -1:
            date = month_num * 100 + day

# set the decoration flags
            spooky = (1003 <= date <= 1105)
            turkey = (1028 <= date <= 1128)
            lights = (1115 <= date <= 1231) or (101 <= date <= 104)
            flags = (621 <= date <= 710)

# Output
            if spooky and turkey:
                print("!Spooky Things and Turkeys!")
            elif turkey and lights:
                print("!Turkeys and Strings of Lights!")
            elif spooky:
                print("!Spooky Things!")
            elif turkey:
                print("!Turkeys!")
            elif lights:
                print("!Strings of Lights!")
            elif flags:
                print("!U.S. Flags!")
            else:
                print("!Personal!")
