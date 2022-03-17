# Morsh

A Bash script to decode/encode morse code. Slightly buggy and very unperformant.

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

### Output text, obfuscation level high, fairytale style

```txt
IT WAS THE BEST OF TIMES IT WAS THE WORST OF TIMES IT WAS THE AGE OF WISDOM IT WAS THE AGE OF FOOLISHNESS IT WAS THE EPOCH OF BELIEF IT WAS THE EPOCH OF INCREDULITY IT WAS THE SEASON OF LIGHT IT WAS THE SEASON OF DARKNESS IT WAS THE SPRING OF HOPE IT WAS THE WINTER OF DESPAIR WE HAD EVERYTHING BEFORE US WE HAD NOTHING BEFORE US WE WERE ALL GOING DIRECT TO HEAVEN WE WERE ALL GOING DIRECT THE OTHER WAY  IN SHORT THE PERIOD WAS SO FAR LIKE THE PRESENT PERIOD THAT SOME OF ITS NOISIEST AUTHORITIES INSISTED ON ITS BEING RECEIVED FOR GOOD OR FOR EVIL IN THE SUPERLATIVE DEGREE OF COMPARISON ONLY E
```

## Todo

- [ ] Fix bugs
- [ ] Handle other DITs than `.` (`*`)
- [ ] Support phonetic alphabets?
