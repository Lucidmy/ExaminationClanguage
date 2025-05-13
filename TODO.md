Before you debug your code to simulation or hardware. you need to do this first.

## Hardware test
if you want to debug your code to hardware. Use comment on segment function
as example:

code line 56 - 65
```bash

        lcd_goto(0,0);  //setkan lcd punya (pos,row)
        lcd_number(counter, DEC, 1);
        lcd_string(" ");
        /* LCD akan display Counter mengikut nombor
         * decimal dengan 1 digit
         */
//        SEGMENT = segment[counter];
        /*output segment akan mengikut setting yang
         * diberi, tapi bersyarat mengikut counter
         */
```

code line 75 - 80
```bash
        counter++;
        lcd_goto(0,0);
        lcd_number(counter, DEC, 1);
        lcd_string(" ");
        //SEGMENT = segment[counter];
        __delay_ms(1000);
```
