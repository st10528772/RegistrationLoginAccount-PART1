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
Open the project in Apache NetBeans and press **F6**, or from the project
folder:
