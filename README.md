# usergen
Small program to generate usernames, such as *AmbitiousParrot2012*, *LonelyPossibility87965* and *HopefulBird7776*. `usergen` offers a cheap, simple and fast way to create large numbers of user names, for example for testing or staging environments.

Without any command line arguments, `usergen` generates a single user name and prints it to `stdout`:
```
$>./usergen
GreenWeekend7438
$>
```
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