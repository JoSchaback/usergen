# usergen - user name generator
Small program to generate usernames, such as _AmbitiousParrot2012_, _LonelyPossibility87965_ and _HopefulBird7776_. 

`usergen` offers a cheap, simple and fast way to create large numbers of user names, for example for testing or staging environments. No
need to burn through your GPT tokens to generate user names 😊.

Without any command line arguments, `usergen` generates a single user name and prints it to `stdout`:
```
$>./usergen
GreenWeekend7438
$>
```
## Pattern
You can provide a pattern to control how the user names are patched together. By default, the standard pattern is `AdjectiveNounNumber4` (see also above). By providing a pattern as command line argument, `usergen` generates different user names. For example, the pattern `the_Adjective_And___Noun`
generates user names of the following forms:
```
$>./usergen the_Adjective_And___Noun -c 5
the_Punctual_And___Bug
the_Comical_And___Dinner
the_Defiant_And___Yard
the_Mawkish_And___Kitchen
the_Quirky_And___Button
$>
```
The `-c 5` parameter tells the program to generate five user names. The following elements are recognized to build patterns:
- `Adjective`: upper case adjective
- `adjective`: lower case adjective
- `Noun`: upper case noun
- `noun`: lower case noun
- `Number`: random number, followed by a single digit to denote the number of digits of the random number
## Options
The following additional options can be used to control the output of `usergen`.
- `-c`, `--count`: number of user names to generate
- `-s`, `--seed`: srand initializer seed number. If not provided, a time-based initialization will be used.
## How to compile
Since `usergen` is a single source file, compiling is trivial:
```
clang usergen.c -o usergen
```
I use `clang` in this case, but any other C compiler should do as well.

## License
Do whatever you want with it. I stole parts of it and you can steal mine too.

## Feedback
If your heart yearns for a feature or improvement, let me know.