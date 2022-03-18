# Morsh

A Bash script to decode/encode morse code. Slightly buggy and very, very slow. Could also be used as an extremely unpleasant way to uppercase text.

## Supplying text

There are three ways to supply input text to this script:

  1) Add a file as argument
  2) Add word or words as arguments
  3) Pipe text to it

In case 2, the script tries to guess the relevant mode, in other cases specify mode with a flag (see below).

## Options

`-d/--decode` - Takes morse code and outputs plain text
`-e/--encode` - Takes plain text and outputs morse code

## Usage examples

Quickly decode a message from some ancient online puzzle game:

```bash
./morsh ...- --- --- -.. --- --- / -- .- --. .. -.-.
```

Awkwardly uppercase a sentence (removing punctuation and fluff in the process):

```bash
echo "I Have No Mouth, and I Must Scream" | ./morsh -e | ./morsh -d
```

Turn Crime and Punishment into something you can reliably broadcast to your entire neighborhood with a simple signal horn and some patience:

```bash
curl https://gutenberg.org/files/2554/2554-0.txt | ./morsh --encode | less
```

## Output examples

### Input text

```txt
It was the best of times, it was the worst of times, it was the age of wisdom, it was the age of foolishness, it was the epoch of belief, it was the epoch of incredulity, it was the season of Light, it was the season of Darkness, it was the spring of hope, it was the winter of despair, we had everything before us, we had nothing before us, we were all going direct to Heaven, we were all going direct the other way – in short, the period was so far like the present period, that some of its noisiest authorities insisted on its being received, for good or for evil, in the superlative degree of comparison only.
```

### Output text

```txt
.. - / .-- .- ... / - .... . / -... . ... - / --- ..-. / - .. -- . ...  / .. - / .-- .- ... / - .... . / .-- --- .-. ... - / --- ..-. / - .. -- . ...  / .. - / .-- .- ... / - .... . / .- --. . / --- ..-. / .-- .. ... -.. --- --  / .. - / .-- .- ... / - .... . / .- --. . / --- ..-. / ..-. --- --- .-.. .. ... .... -. . ... ...  / .. - / .-- .- ... / - .... . / . .--. --- -.-. .... / --- ..-. / -... . .-.. .. . ..-.  / .. - / .-- .- ... / - .... . / . .--. --- -.-. .... / --- ..-. / .. -. -.-. .-. . -.. ..- .-.. .. - -.--  / .. - / .-- .- ... / - .... . / ... . .- ... --- -. / --- ..-. / .-.. .. --. .... -  / .. - / .-- .- ... / - .... . / ... . .- ... --- -. / --- ..-. / -.. .- .-. -.- -. . ... ...  / .. - / .-- .- ... / - .... . / ... .--. .-. .. -. --. / --- ..-. / .... --- .--. .  / .. - / .-- .- ... / - .... . / .-- .. -. - . .-. / --- ..-. / -.. . ... .--. .- .. .-.  / .-- . / .... .- -.. / . ...- . .-. -.-- - .... .. -. --. / -... . ..-. --- .-. . / ..- ...  / .-- . / .... .- -.. / -. --- - .... .. -. --. / -... . ..-. --- .-. . / ..- ...  / .-- . / .-- . .-. . / .- .-.. .-.. / --. --- .. -. --. / -.. .. .-. . -.-. - / - --- / .... . .- ...- . -.  / .-- . / .-- . .-. . / .- .-.. .-.. / --. --- .. -. --. / -.. .. .-. . -.-. - / - .... . / --- - .... . .-. / .-- .- -.-- /  / .. -. / ... .... --- .-. -  / - .... . / .--. . .-. .. --- -.. / .-- .- ... / ... --- / ..-. .- .-. / .-.. .. -.- . / - .... . / .--. .-. . ... . -. - / .--. . .-. .. --- -..  / - .... .- - / ... --- -- . / --- ..-. / .. - ... / -. --- .. ... .. . ... - / .- ..- - .... --- .-. .. - .. . ... / .. -. ... .. ... - . -.. / --- -. / .. - ... / -... . .. -. --. / .-. . -.-. . .. ...- . -..  / ..-. --- .-. / --. --- --- -.. / --- .-. / ..-. --- .-. / . ...- .. .-..  / .. -. / - .... . / ... ..- .--. . .-. .-.. .- - .. ...- . / -.. . --. .-. . . / --- ..-. / -.-. --- -- .--. .- .-. .. ... --- -. / --- -. .-.. -.-- ./
```

### Input text

```txt
.. - / .-- .- ... / - .... . / -... . ... - / --- ..-. / - .. -- . ...  / .. - / .-- .- ... / - .... . / .-- --- .-. ... - / --- ..-. / - .. -- . ...  / .. - / .-- .- ... / - .... . / .- --. . / --- ..-. / .-- .. ... -.. --- --  / .. - / .-- .- ... / - .... . / .- --. . / --- ..-. / ..-. --- --- .-.. .. ... .... -. . ... ...  / .. - / .-- .- ... / - .... . / . .--. --- -.-. .... / --- ..-. / -... . .-.. .. . ..-.  / .. - / .-- .- ... / - .... . / . .--. --- -.-. .... / --- ..-. / .. -. -.-. .-. . -.. ..- .-.. .. - -.--  / .. - / .-- .- ... / - .... . / ... . .- ... --- -. / --- ..-. / .-.. .. --. .... -  / .. - / .-- .- ... / - .... . / ... . .- ... --- -. / --- ..-. / -.. .- .-. -.- -. . ... ...  / .. - / .-- .- ... / - .... . / ... .--. .-. .. -. --. / --- ..-. / .... --- .--. .  / .. - / .-- .- ... / - .... . / .-- .. -. - . .-. / --- ..-. / -.. . ... .--. .- .. .-.  / .-- . / .... .- -.. / . ...- . .-. -.-- - .... .. -. --. / -... . ..-. --- .-. . / ..- ...  / .-- . / .... .- -.. / -. --- - .... .. -. --. / -... . ..-. --- .-. . / ..- ...  / .-- . / .-- . .-. . / .- .-.. .-.. / --. --- .. -. --. / -.. .. .-. . -.-. - / - --- / .... . .- ...- . -.  / .-- . / .-- . .-. . / .- .-.. .-.. / --. --- .. -. --. / -.. .. .-. . -.-. - / - .... . / --- - .... . .-. / .-- .- -.-- /  / .. -. / ... .... --- .-. -  / - .... . / .--. . .-. .. --- -.. / .-- .- ... / ... --- / ..-. .- .-. / .-.. .. -.- . / - .... . / .--. .-. . ... . -. - / .--. . .-. .. --- -..  / - .... .- - / ... --- -- . / --- ..-. / .. - ... / -. --- .. ... .. . ... - / .- ..- - .... --- .-. .. - .. . ... / .. -. ... .. ... - . -.. / --- -. / .. - ... / -... . .. -. --. / .-. . -.-. . .. ...- . -..  / ..-. --- .-. / --. --- --- -.. / --- .-. / ..-. --- .-. / . ...- .. .-..  / .. -. / - .... . / ... ..- .--. . .-. .-.. .- - .. ...- . / -.. . --. .-. . . / --- ..-. / -.-. --- -- .--. .- .-. .. ... --- -. / --- -. .-.. -.-- ./
```

### Output text

```txt
IT WAS THE BEST OF TIMES IT WAS THE WORST OF TIMES IT WAS THE AGE OF WISDOM IT WAS THE AGE OF FOOLISHNESS IT WAS THE EPOCH OF BELIEF IT WAS THE EPOCH OF INCREDULITY IT WAS THE SEASON OF LIGHT IT WAS THE SEASON OF DARKNESS IT WAS THE SPRING OF HOPE IT WAS THE WINTER OF DESPAIR WE HAD EVERYTHING BEFORE US WE HAD NOTHING BEFORE US WE WERE ALL GOING DIRECT TO HEAVEN WE WERE ALL GOING DIRECT THE OTHER WAY  IN SHORT THE PERIOD WAS SO FAR LIKE THE PRESENT PERIOD THAT SOME OF ITS NOISIEST AUTHORITIES INSISTED ON ITS BEING RECEIVED FOR GOOD OR FOR EVIL IN THE SUPERLATIVE DEGREE OF COMPARISON ONLY
```

## Todo

- [ ] Handle spaces when piping
- [ ] Handle other DITs than `.` (`*`) <-- Hey, that’s not very linuxy
- [ ] Move mode guessing to `handle_line` so we can support in with all input models
- [ ] Convert things like `é` to `e` before encoding
- [ ] Support phonetic alphabets?
- [ ] Clean up output text (no traling `/`, no extra newline)
- [x] Remove dots from plain text
