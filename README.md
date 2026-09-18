# Registration and Login Account

PROG5121 Programming 1A · Portfolio of Evidence Part 1  
Palesa · Dikolane · ST10528772

## About

A Java console application that registers a user and then allows them to
log in. All validation rules and account data are held in the `Login`
class, separately from the console interface, so that the rules can be
tested on their own.

## Validation rules

| Field | Rule |
|-------|------|
| Username | Must contain an underscore and be no longer than five characters |
| Password | At least eight characters, including a capital letter, a number and a special character |
| Cell phone number | South African international format — `+27` followed by nine digits |

## Project structure

| File | Purpose |
|------|---------|
| `RegistrationLoginAccount.java` | Console interface — prompts for details and displays results |
| `Login.java` | Validation rules, registration and login logic |
| `LoginTest.java` | 23 JUnit tests covering every method |

## How it works

The three validation methods in `Login` are `static`, so the console
class can check each field as it is entered without needing an object
yet. The user re-enters a field until it passes, which is why each
prompt sits inside a `while` loop.

Once all three fields are valid, a `Login` object is created and
`registerUser()` confirms the registration. `loginUser()` then compares
the credentials entered at the login prompt against the stored ones, and
`returnLoginStatus()` turns that result into the message shown to the
user.

## Running it

## Testing

23 unit tests written with JUnit, covering valid input, invalid input and
empty input for each rule, plus registration and login outcomes:

## Built with

- Java
- Apache NetBeans
- Apache Ant
- JUnit

## References

Farrell, J., 2023. *Java Programming*. 10th ed. Boston: Cengage Learning.

JUnit Team, 2026. *JUnit 4 Documentation*. [Online]  
Available at: https://junit.org/junit4/  
[Accessed 18 September 2026].

Oracle, 2023. *Class Pattern*. [Online]  
Available at: https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html  
[Accessed 18 September 2026].

Oracle, 2023. *Class Scanner*. [Online]  
Available at: https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/Scanner.html  
[Accessed 18 September 2026].

## Explanation on the code's functionality

The program consists of three files, the registration login account class, the login class and the login test class. In the login, the username must have an underscore and be less than five characters. With the password, it needs to be 8 characters, with a capital letter, a number and a special character. Lastly, with the cellphone number, it must start with South African country code (+27), followed by 9 digits. If all are correctly formatted, the register User will return "user registered successfully", if not it will return that the user was not successfully registered. In the registration login account, it asks for user details. Each prompt has its own loop, so if the input is wrong it outputs an error and requests for what's correct until what the user entered is right. Once everything is validated, the user is then successfully registered and asks them for their login details. If the username and password match the username and password entered at first, it prints a welcome message, if not, incorrect details will be displayed. If I enter a wrong username, that username will be rejected, and I'll be asked to try again. But if I now enter a valid username, I will proceed with the registration by entering the password and the cellphone number. Registration will then succeed; I log in and receive the welcome message. The last program is the test units, which are 20 in number, and they cover each rule that pass or fail. This is how the program functions. Thank you.
Open the project in Apache NetBeans and press **F6**, or from the project
folder:
