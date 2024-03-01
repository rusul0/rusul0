$ checksec mirror
[*] '/home/user/htb-unictf-2020/mirror/mirror'
    Arch:     amd64-64-little
    RELRO:    Full RELRO
    Stack:    No canary found
    NX:       NX enabled
    PIE:      PIE enabled
    $./mirror 
✨ This old mirror seems to contain some hidden power..✨
There is a writing at the bottom of it..
"The mirror will reveal whatever you desire the most.. Just talk to it.."
Do you want to talk to the mirror? (y/n)
> y
Your answer was: y
"This is a gift from the craftsman.. [0x7fffc981ee10] [0x7f5114366c50]"
Now you can talk to the mirror.
> hello there
>
> undefined8 main(void) {
  undefined8 local_28, local_20, local_18, local_10;
  
  setup();
  local_28 = 0; local_20 = 0; local_18 = 0; local_10 = 0;
  puts(&DAT_00102068);
  puts("\"The mirror will reveal whatever you desire the most.. Just talk to it..\"");
  printf("Do you want to talk to the mirror? (y/n)\n> ");
  read(0,&local_28,0x1f);
  if (((char)local_28 != 'y') && ((char)local_28 != 'Y')) {
    puts("You left the abandoned house safe!");
                    /* WARNING: Subroutine does not return */
    exit(0x45);
  }
  printf("Your answer was: ");
  printf((char *)&local_28);
  reveal();
  return 0;
}
undefined8 main(void) {
  undefined8 local_28, local_20, local_18, local_10;
  
  setup();
  local_28 = 0; local_20 = 0; local_18 = 0; local_10 = 0;
  puts(&DAT_00102068);
  puts("\"The mirror will reveal whatever you desire the most.. Just talk to it..\"");
  printf("Do you want to talk to the mirror? (y/n)\n> ");
  read(0,&local_28,0x1f);
  if (((char)local_28 != 'y') && ((char)local_28 != 'Y')) {
    puts("You left the abandoned house safe!");
                    /* WARNING: Subroutine does not return */
    exit(0x45);
  }
  printf("Your answer was: ");
  printf((char *)&local_28);
  reveal();
  return 0;
}
leave
ret              # return to main+199
mov    eax,0x0
leave
ret
