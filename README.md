# kaktovik-watch
source code and notes for the kaktovik watch as published on google play
As created on Watch Face Studio (WFS) 

## Notes on WFS Tags Expressions (That they don't tell you in the documentation)
- Custom bitmap fonts must be refered to in a specific manner. For the bitmap icon `digit_0`, it must be referenced as `"[digit_0]"` with both brackets and quotes to be considered a valid string.
- All "Tags", which are system variables as provided by the WFS, must be inside of brackets in order to be valid.
- All calculations must have an additional parentheses surrounding the calculation in order to be considered a calculation and not just a really long string
- ChatGPT has no idea how to code in WFS, don't bother asking unless you're prepared to just use it as pseudo-code, as it doesn't seem to have any knowledge of how WFS works.


## Code

### Ikarraq
```
(([SEC_IN_DAY] / 86400) * 20 < 1 ? "[digit_0]" : (([SEC_IN_DAY] / 86400) * 20 < 2 ? "[digit_1]" : (([SEC_IN_DAY] / 86400) * 20 < 3 ? "[digit_2]" : (([SEC_IN_DAY] / 86400) * 20 < 4 ? "[digit_3]" : (([SEC_IN_DAY] / 86400) * 20 < 5 ? "[digit_4]" : (([SEC_IN_DAY] / 86400) * 20 < 6 ? "[digit_5]" : (([SEC_IN_DAY] / 86400) * 20 < 7 ? "[digit_6]" : (([SEC_IN_DAY] / 86400) * 20 < 8 ? "[digit_7]" : (([SEC_IN_DAY] / 86400) * 20 < 9 ? "[digit_8]" : (([SEC_IN_DAY] / 86400) * 20 < 10 ? "[digit_9]" : (([SEC_IN_DAY] / 86400) * 20 < 11 ? "[digit_10]" : (([SEC_IN_DAY] / 86400) * 20 < 12 ? "[digit_11]" : (([SEC_IN_DAY] / 86400) * 20 < 13 ? "[digit_12]" : (([SEC_IN_DAY] / 86400) * 20 < 14 ? "[digit_13]" : (([SEC_IN_DAY] / 86400) * 20 < 15 ? "[digit_14]" : (([SEC_IN_DAY] / 86400) * 20 < 16 ? "[digit_15]" : (([SEC_IN_DAY] / 86400) * 20 < 17 ? "[digit_16]" : (([SEC_IN_DAY] / 86400) * 20 < 18 ? "[digit_17]" : (([SEC_IN_DAY] / 86400) * 20 < 19 ? "[digit_18]" : (([SEC_IN_DAY] / 86400) * 20 < 20 ? "[digit_19]" : "error"))))))))))))))))))))
```

### Mein
```
((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 1 ? "[digit_0]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 2 ? "[digit_1]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 3 ? "[digit_2]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 4 ? "[digit_3]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 5 ? "[digit_4]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 6 ? "[digit_5]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 7 ? "[digit_6]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 8 ? "[digit_7]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 9 ? "[digit_8]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 10 ? "[digit_9]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 11 ? "[digit_10]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 12 ? "[digit_11]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 13 ? "[digit_12]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 14 ? "[digit_13]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 15 ? "[digit_14]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 16 ? "[digit_15]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 17 ? "[digit_16]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 18 ? "[digit_17]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) < 19 ? "[digit_18]" : ((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) <= 20.1 ? "[digit_19]" : "error"))))))))))))))))))))
```

### Tick
```
((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 1 ? "[digit_0]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 2 ? "[digit_1]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 3 ? "[digit_2]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 4 ? "[digit_3]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 5 ? "[digit_4]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 6 ? "[digit_5]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 7 ? "[digit_6]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 8 ? "[digit_7]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 9 ? "[digit_8]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 10 ? "[digit_9]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 11 ? "[digit_10]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 12 ? "[digit_11]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 13 ? "[digit_12]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 14 ? "[digit_13]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 15 ? "[digit_14]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 16 ? "[digit_15]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 17 ? "[digit_16]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 18 ? "[digit_17]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 19 ? "[digit_18]" : ((((((([SEC_IN_DAY] / 86400) * 20) % 1) * 20) % 1) * 20) < 20 ? "[digit_19]" : "error"))))))))))))))))))))
```

