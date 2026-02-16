THis card provide 2 functionality :  
- duplicates the card slot into 2 horizontal slots
- rom emulation card (https://mirrors.apple2.org.za/ftp.apple.asimov.net/documentation/hardware/schematics/rom_emulator_card_050-0009-01_schematic.pdf)

# Slot doubler  
This card is designed to allow the installation of two cards in a single slot. Although it can be installed in any slot, it is most effectively used as a splitter in slot 7. Since the two connectors are wired in parallel, not all card combinations are possible.
## kind of card
We can identify 3 kind of cards :
- basic card who use soft switch (16 address C080+n) to interact whith the system, ioselect line is used
- card with firmware locate at Cn00-CnFF (n=0 to 7), icprobe is used
- card "watching" the address bus (did'nt use ioselect, ioprobe or devices select) 

## 
usefull information can be fund here : https://grokipedia.com/page/apple_ii_peripheral_cards

# Rom emulation card
The rom is activated when a jumper is set on JP4. Current version can only by used for Apple II deadtest ROM (https://github.com/misterblack1/appleII_deadtest). Work is in progress to be emulate all functionalities of Apple Rom Emulator Card ([050-0009-01](https://mirrors.apple2.org.za/Apple%20II%20Documentation%20Project/Interface%20Cards/ROM%20Cards/Apple%20ROM%20Emulator%20Card/Photos/Apple%20ROM%20Card%20with%20ROM%20-%20Front.jpg))
but with only one Rom chip (27128).
