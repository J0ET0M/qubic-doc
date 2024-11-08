# ComputorIndex

The ComputorIndex deines the index of a computor in a range from 0 to 675.

The list of [Computors](Computor.md) is a sorted list of [Qubic Id's](Qubic_Id.md) which can be translated to their Shortcode.

The logic to convert between Index and ShortCode is:

```c#
 public static string ComputorShortCode(int index)
 {
     char[] alphabet = { 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z' };
     return alphabet[index / 26].ToString() + alphabet[index % 26].ToString();
 }

 public static ushort ReverseComputorShortCode(string shortCode)
 {
     char[] alphabet = { 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z' };
     if (shortCode.Length != 2)
     {
         throw new ArgumentException("Invalid short code format. The short code must be exactly two characters long.");
     }

     char firstChar = shortCode[0];
     char secondChar = shortCode[1];

     int firstIndex = Array.IndexOf(alphabet, char.ToUpper(firstChar));
     int secondIndex = Array.IndexOf(alphabet, char.ToUpper(secondChar));

     if (firstIndex < 0 || secondIndex < 0)
     {
         throw new ArgumentException("Invalid characters in the short code.");
     }

     return (ushort)(firstIndex * 26 + secondIndex);
 }

```

# Appendix: Computor indices

|  Index 	| ShortCode  	| 
|---	|---	|
 | 0 | AA | 
 | 1 | AB | 
 | 2 | AC | 
 | 3 | AD | 
 | 4 | AE | 
 | 5 | AF | 
 | 6 | AG | 
 | 7 | AH | 
 | 8 | AI | 
 | 9 | AJ | 
 | 10 | AK | 
 | 11 | AL | 
 | 12 | AM | 
 | 13 | AN | 
 | 14 | AO | 
 | 15 | AP | 
 | 16 | AQ | 
 | 17 | AR | 
 | 18 | AS | 
 | 19 | AT | 
 | 20 | AU | 
 | 21 | AV | 
 | 22 | AW | 
 | 23 | AX | 
 | 24 | AY | 
 | 25 | AZ | 
 | 26 | BA | 
 | 27 | BB | 
 | 28 | BC | 
 | 29 | BD | 
 | 30 | BE | 
 | 31 | BF | 
 | 32 | BG | 
 | 33 | BH | 
 | 34 | BI | 
 | 35 | BJ | 
 | 36 | BK | 
 | 37 | BL | 
 | 38 | BM | 
 | 39 | BN | 
 | 40 | BO | 
 | 41 | BP | 
 | 42 | BQ | 
 | 43 | BR | 
 | 44 | BS | 
 | 45 | BT | 
 | 46 | BU | 
 | 47 | BV | 
 | 48 | BW | 
 | 49 | BX | 
 | 50 | BY | 
 | 51 | BZ | 
 | 52 | CA | 
 | 53 | CB | 
 | 54 | CC | 
 | 55 | CD | 
 | 56 | CE | 
 | 57 | CF | 
 | 58 | CG | 
 | 59 | CH | 
 | 60 | CI | 
 | 61 | CJ | 
 | 62 | CK | 
 | 63 | CL | 
 | 64 | CM | 
 | 65 | CN | 
 | 66 | CO | 
 | 67 | CP | 
 | 68 | CQ | 
 | 69 | CR | 
 | 70 | CS | 
 | 71 | CT | 
 | 72 | CU | 
 | 73 | CV | 
 | 74 | CW | 
 | 75 | CX | 
 | 76 | CY | 
 | 77 | CZ | 
 | 78 | DA | 
 | 79 | DB | 
 | 80 | DC | 
 | 81 | DD | 
 | 82 | DE | 
 | 83 | DF | 
 | 84 | DG | 
 | 85 | DH | 
 | 86 | DI | 
 | 87 | DJ | 
 | 88 | DK | 
 | 89 | DL | 
 | 90 | DM | 
 | 91 | DN | 
 | 92 | DO | 
 | 93 | DP | 
 | 94 | DQ | 
 | 95 | DR | 
 | 96 | DS | 
 | 97 | DT | 
 | 98 | DU | 
 | 99 | DV | 
 | 100 | DW | 
 | 101 | DX | 
 | 102 | DY | 
 | 103 | DZ | 
 | 104 | EA | 
 | 105 | EB | 
 | 106 | EC | 
 | 107 | ED | 
 | 108 | EE | 
 | 109 | EF | 
 | 110 | EG | 
 | 111 | EH | 
 | 112 | EI | 
 | 113 | EJ | 
 | 114 | EK | 
 | 115 | EL | 
 | 116 | EM | 
 | 117 | EN | 
 | 118 | EO | 
 | 119 | EP | 
 | 120 | EQ | 
 | 121 | ER | 
 | 122 | ES | 
 | 123 | ET | 
 | 124 | EU | 
 | 125 | EV | 
 | 126 | EW | 
 | 127 | EX | 
 | 128 | EY | 
 | 129 | EZ | 
 | 130 | FA | 
 | 131 | FB | 
 | 132 | FC | 
 | 133 | FD | 
 | 134 | FE | 
 | 135 | FF | 
 | 136 | FG | 
 | 137 | FH | 
 | 138 | FI | 
 | 139 | FJ | 
 | 140 | FK | 
 | 141 | FL | 
 | 142 | FM | 
 | 143 | FN | 
 | 144 | FO | 
 | 145 | FP | 
 | 146 | FQ | 
 | 147 | FR | 
 | 148 | FS | 
 | 149 | FT | 
 | 150 | FU | 
 | 151 | FV | 
 | 152 | FW | 
 | 153 | FX | 
 | 154 | FY | 
 | 155 | FZ | 
 | 156 | GA | 
 | 157 | GB | 
 | 158 | GC | 
 | 159 | GD | 
 | 160 | GE | 
 | 161 | GF | 
 | 162 | GG | 
 | 163 | GH | 
 | 164 | GI | 
 | 165 | GJ | 
 | 166 | GK | 
 | 167 | GL | 
 | 168 | GM | 
 | 169 | GN | 
 | 170 | GO | 
 | 171 | GP | 
 | 172 | GQ | 
 | 173 | GR | 
 | 174 | GS | 
 | 175 | GT | 
 | 176 | GU | 
 | 177 | GV | 
 | 178 | GW | 
 | 179 | GX | 
 | 180 | GY | 
 | 181 | GZ | 
 | 182 | HA | 
 | 183 | HB | 
 | 184 | HC | 
 | 185 | HD | 
 | 186 | HE | 
 | 187 | HF | 
 | 188 | HG | 
 | 189 | HH | 
 | 190 | HI | 
 | 191 | HJ | 
 | 192 | HK | 
 | 193 | HL | 
 | 194 | HM | 
 | 195 | HN | 
 | 196 | HO | 
 | 197 | HP | 
 | 198 | HQ | 
 | 199 | HR | 
 | 200 | HS | 
 | 201 | HT | 
 | 202 | HU | 
 | 203 | HV | 
 | 204 | HW | 
 | 205 | HX | 
 | 206 | HY | 
 | 207 | HZ | 
 | 208 | IA | 
 | 209 | IB | 
 | 210 | IC | 
 | 211 | ID | 
 | 212 | IE | 
 | 213 | IF | 
 | 214 | IG | 
 | 215 | IH | 
 | 216 | II | 
 | 217 | IJ | 
 | 218 | IK | 
 | 219 | IL | 
 | 220 | IM | 
 | 221 | IN | 
 | 222 | IO | 
 | 223 | IP | 
 | 224 | IQ | 
 | 225 | IR | 
 | 226 | IS | 
 | 227 | IT | 
 | 228 | IU | 
 | 229 | IV | 
 | 230 | IW | 
 | 231 | IX | 
 | 232 | IY | 
 | 233 | IZ | 
 | 234 | JA | 
 | 235 | JB | 
 | 236 | JC | 
 | 237 | JD | 
 | 238 | JE | 
 | 239 | JF | 
 | 240 | JG | 
 | 241 | JH | 
 | 242 | JI | 
 | 243 | JJ | 
 | 244 | JK | 
 | 245 | JL | 
 | 246 | JM | 
 | 247 | JN | 
 | 248 | JO | 
 | 249 | JP | 
 | 250 | JQ | 
 | 251 | JR | 
 | 252 | JS | 
 | 253 | JT | 
 | 254 | JU | 
 | 255 | JV | 
 | 256 | JW | 
 | 257 | JX | 
 | 258 | JY | 
 | 259 | JZ | 
 | 260 | KA | 
 | 261 | KB | 
 | 262 | KC | 
 | 263 | KD | 
 | 264 | KE | 
 | 265 | KF | 
 | 266 | KG | 
 | 267 | KH | 
 | 268 | KI | 
 | 269 | KJ | 
 | 270 | KK | 
 | 271 | KL | 
 | 272 | KM | 
 | 273 | KN | 
 | 274 | KO | 
 | 275 | KP | 
 | 276 | KQ | 
 | 277 | KR | 
 | 278 | KS | 
 | 279 | KT | 
 | 280 | KU | 
 | 281 | KV | 
 | 282 | KW | 
 | 283 | KX | 
 | 284 | KY | 
 | 285 | KZ | 
 | 286 | LA | 
 | 287 | LB | 
 | 288 | LC | 
 | 289 | LD | 
 | 290 | LE | 
 | 291 | LF | 
 | 292 | LG | 
 | 293 | LH | 
 | 294 | LI | 
 | 295 | LJ | 
 | 296 | LK | 
 | 297 | LL | 
 | 298 | LM | 
 | 299 | LN | 
 | 300 | LO | 
 | 301 | LP | 
 | 302 | LQ | 
 | 303 | LR | 
 | 304 | LS | 
 | 305 | LT | 
 | 306 | LU | 
 | 307 | LV | 
 | 308 | LW | 
 | 309 | LX | 
 | 310 | LY | 
 | 311 | LZ | 
 | 312 | MA | 
 | 313 | MB | 
 | 314 | MC | 
 | 315 | MD | 
 | 316 | ME | 
 | 317 | MF | 
 | 318 | MG | 
 | 319 | MH | 
 | 320 | MI | 
 | 321 | MJ | 
 | 322 | MK | 
 | 323 | ML | 
 | 324 | MM | 
 | 325 | MN | 
 | 326 | MO | 
 | 327 | MP | 
 | 328 | MQ | 
 | 329 | MR | 
 | 330 | MS | 
 | 331 | MT | 
 | 332 | MU | 
 | 333 | MV | 
 | 334 | MW | 
 | 335 | MX | 
 | 336 | MY | 
 | 337 | MZ | 
 | 338 | NA | 
 | 339 | NB | 
 | 340 | NC | 
 | 341 | ND | 
 | 342 | NE | 
 | 343 | NF | 
 | 344 | NG | 
 | 345 | NH | 
 | 346 | NI | 
 | 347 | NJ | 
 | 348 | NK | 
 | 349 | NL | 
 | 350 | NM | 
 | 351 | NN | 
 | 352 | NO | 
 | 353 | NP | 
 | 354 | NQ | 
 | 355 | NR | 
 | 356 | NS | 
 | 357 | NT | 
 | 358 | NU | 
 | 359 | NV | 
 | 360 | NW | 
 | 361 | NX | 
 | 362 | NY | 
 | 363 | NZ | 
 | 364 | OA | 
 | 365 | OB | 
 | 366 | OC | 
 | 367 | OD | 
 | 368 | OE | 
 | 369 | OF | 
 | 370 | OG | 
 | 371 | OH | 
 | 372 | OI | 
 | 373 | OJ | 
 | 374 | OK | 
 | 375 | OL | 
 | 376 | OM | 
 | 377 | ON | 
 | 378 | OO | 
 | 379 | OP | 
 | 380 | OQ | 
 | 381 | OR | 
 | 382 | OS | 
 | 383 | OT | 
 | 384 | OU | 
 | 385 | OV | 
 | 386 | OW | 
 | 387 | OX | 
 | 388 | OY | 
 | 389 | OZ | 
 | 390 | PA | 
 | 391 | PB | 
 | 392 | PC | 
 | 393 | PD | 
 | 394 | PE | 
 | 395 | PF | 
 | 396 | PG | 
 | 397 | PH | 
 | 398 | PI | 
 | 399 | PJ | 
 | 400 | PK | 
 | 401 | PL | 
 | 402 | PM | 
 | 403 | PN | 
 | 404 | PO | 
 | 405 | PP | 
 | 406 | PQ | 
 | 407 | PR | 
 | 408 | PS | 
 | 409 | PT | 
 | 410 | PU | 
 | 411 | PV | 
 | 412 | PW | 
 | 413 | PX | 
 | 414 | PY | 
 | 415 | PZ | 
 | 416 | QA | 
 | 417 | QB | 
 | 418 | QC | 
 | 419 | QD | 
 | 420 | QE | 
 | 421 | QF | 
 | 422 | QG | 
 | 423 | QH | 
 | 424 | QI | 
 | 425 | QJ | 
 | 426 | QK | 
 | 427 | QL | 
 | 428 | QM | 
 | 429 | QN | 
 | 430 | QO | 
 | 431 | QP | 
 | 432 | QQ | 
 | 433 | QR | 
 | 434 | QS | 
 | 435 | QT | 
 | 436 | QU | 
 | 437 | QV | 
 | 438 | QW | 
 | 439 | QX | 
 | 440 | QY | 
 | 441 | QZ | 
 | 442 | RA | 
 | 443 | RB | 
 | 444 | RC | 
 | 445 | RD | 
 | 446 | RE | 
 | 447 | RF | 
 | 448 | RG | 
 | 449 | RH | 
 | 450 | RI | 
 | 451 | RJ | 
 | 452 | RK | 
 | 453 | RL | 
 | 454 | RM | 
 | 455 | RN | 
 | 456 | RO | 
 | 457 | RP | 
 | 458 | RQ | 
 | 459 | RR | 
 | 460 | RS | 
 | 461 | RT | 
 | 462 | RU | 
 | 463 | RV | 
 | 464 | RW | 
 | 465 | RX | 
 | 466 | RY | 
 | 467 | RZ | 
 | 468 | SA | 
 | 469 | SB | 
 | 470 | SC | 
 | 471 | SD | 
 | 472 | SE | 
 | 473 | SF | 
 | 474 | SG | 
 | 475 | SH | 
 | 476 | SI | 
 | 477 | SJ | 
 | 478 | SK | 
 | 479 | SL | 
 | 480 | SM | 
 | 481 | SN | 
 | 482 | SO | 
 | 483 | SP | 
 | 484 | SQ | 
 | 485 | SR | 
 | 486 | SS | 
 | 487 | ST | 
 | 488 | SU | 
 | 489 | SV | 
 | 490 | SW | 
 | 491 | SX | 
 | 492 | SY | 
 | 493 | SZ | 
 | 494 | TA | 
 | 495 | TB | 
 | 496 | TC | 
 | 497 | TD | 
 | 498 | TE | 
 | 499 | TF | 
 | 500 | TG | 
 | 501 | TH | 
 | 502 | TI | 
 | 503 | TJ | 
 | 504 | TK | 
 | 505 | TL | 
 | 506 | TM | 
 | 507 | TN | 
 | 508 | TO | 
 | 509 | TP | 
 | 510 | TQ | 
 | 511 | TR | 
 | 512 | TS | 
 | 513 | TT | 
 | 514 | TU | 
 | 515 | TV | 
 | 516 | TW | 
 | 517 | TX | 
 | 518 | TY | 
 | 519 | TZ | 
 | 520 | UA | 
 | 521 | UB | 
 | 522 | UC | 
 | 523 | UD | 
 | 524 | UE | 
 | 525 | UF | 
 | 526 | UG | 
 | 527 | UH | 
 | 528 | UI | 
 | 529 | UJ | 
 | 530 | UK | 
 | 531 | UL | 
 | 532 | UM | 
 | 533 | UN | 
 | 534 | UO | 
 | 535 | UP | 
 | 536 | UQ | 
 | 537 | UR | 
 | 538 | US | 
 | 539 | UT | 
 | 540 | UU | 
 | 541 | UV | 
 | 542 | UW | 
 | 543 | UX | 
 | 544 | UY | 
 | 545 | UZ | 
 | 546 | VA | 
 | 547 | VB | 
 | 548 | VC | 
 | 549 | VD | 
 | 550 | VE | 
 | 551 | VF | 
 | 552 | VG | 
 | 553 | VH | 
 | 554 | VI | 
 | 555 | VJ | 
 | 556 | VK | 
 | 557 | VL | 
 | 558 | VM | 
 | 559 | VN | 
 | 560 | VO | 
 | 561 | VP | 
 | 562 | VQ | 
 | 563 | VR | 
 | 564 | VS | 
 | 565 | VT | 
 | 566 | VU | 
 | 567 | VV | 
 | 568 | VW | 
 | 569 | VX | 
 | 570 | VY | 
 | 571 | VZ | 
 | 572 | WA | 
 | 573 | WB | 
 | 574 | WC | 
 | 575 | WD | 
 | 576 | WE | 
 | 577 | WF | 
 | 578 | WG | 
 | 579 | WH | 
 | 580 | WI | 
 | 581 | WJ | 
 | 582 | WK | 
 | 583 | WL | 
 | 584 | WM | 
 | 585 | WN | 
 | 586 | WO | 
 | 587 | WP | 
 | 588 | WQ | 
 | 589 | WR | 
 | 590 | WS | 
 | 591 | WT | 
 | 592 | WU | 
 | 593 | WV | 
 | 594 | WW | 
 | 595 | WX | 
 | 596 | WY | 
 | 597 | WZ | 
 | 598 | XA | 
 | 599 | XB | 
 | 600 | XC | 
 | 601 | XD | 
 | 602 | XE | 
 | 603 | XF | 
 | 604 | XG | 
 | 605 | XH | 
 | 606 | XI | 
 | 607 | XJ | 
 | 608 | XK | 
 | 609 | XL | 
 | 610 | XM | 
 | 611 | XN | 
 | 612 | XO | 
 | 613 | XP | 
 | 614 | XQ | 
 | 615 | XR | 
 | 616 | XS | 
 | 617 | XT | 
 | 618 | XU | 
 | 619 | XV | 
 | 620 | XW | 
 | 621 | XX | 
 | 622 | XY | 
 | 623 | XZ | 
 | 624 | YA | 
 | 625 | YB | 
 | 626 | YC | 
 | 627 | YD | 
 | 628 | YE | 
 | 629 | YF | 
 | 630 | YG | 
 | 631 | YH | 
 | 632 | YI | 
 | 633 | YJ | 
 | 634 | YK | 
 | 635 | YL | 
 | 636 | YM | 
 | 637 | YN | 
 | 638 | YO | 
 | 639 | YP | 
 | 640 | YQ | 
 | 641 | YR | 
 | 642 | YS | 
 | 643 | YT | 
 | 644 | YU | 
 | 645 | YV | 
 | 646 | YW | 
 | 647 | YX | 
 | 648 | YY | 
 | 649 | YZ | 
 | 650 | ZA | 
 | 651 | ZB | 
 | 652 | ZC | 
 | 653 | ZD | 
 | 654 | ZE | 
 | 655 | ZF | 
 | 656 | ZG | 
 | 657 | ZH | 
 | 658 | ZI | 
 | 659 | ZJ | 
 | 660 | ZK | 
 | 661 | ZL | 
 | 662 | ZM | 
 | 663 | ZN | 
 | 664 | ZO | 
 | 665 | ZP | 
 | 666 | ZQ | 
 | 667 | ZR | 
 | 668 | ZS | 
 | 669 | ZT | 
 | 670 | ZU | 
 | 671 | ZV | 
 | 672 | ZW | 
 | 673 | ZX | 
 | 674 | ZY | 
 | 675 | ZZ | 

