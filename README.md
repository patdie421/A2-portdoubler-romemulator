This card provide 2 functionality :  
- duplicates the card slot into 2 horizontal slots. I imagened this card to be able to use a A2DVI in Apple IIs that all slots are used.  
- rom emulation card (https://mirrors.apple2.org.za/ftp.apple.asimov.net/documentation/hardware/schematics/rom_emulator_card_050-0009-01_schematic.pdf). This first version is designed to use Adrian Black Deadtest ROM (https://github.com/misterblack1/appleII_deadtest)
  - This fist version did'nt allow to control by softwitch
  - DMA IN/OUT are not supported
# Slot doubler  
This card is designed to allow the installation of two cards in a single slot. Although it can be installed in any slot, it is most effectively used as a splitter in slot 7. Since the two connectors are wired in parallel, not all card combinations are possible.
## kinds of Apple II cards
We can identify 3 kinds of cards :
- basic card : use soft switches, 16 addresses 0xC080+n\*0x10 to 0xC08F+n\*0x10, n=1 to 7, to interact whith the system. The card is activated by "Device Select" line.
- card with firmware locate at Cn00-CnFF (n=1 to 7), the "I/O Select" activated this kind of card when the firmware page is read or write. Most of this cards (if not all) use also soft switches at addresses C0N0x.  
- card "watching" the address bus (did'nt use Device Select or or I/O Select).  

Other factors limit this combination, including the use of DMA and interrupt lines (/NMI and /INT).  

Before trying to install 2 cards in the doubled slots you have to know witch kind of cards you have.  
 
## possible combinaisons

## working (tested) combinaisons
(to be done)

(usefull information can be fund here : https://grokipedia.com/page/apple_ii_peripheral_cards)

# Rom emulation card
The rom is activated when a jumper is set on JP4. Current version can only by used for Apple II deadtest ROM (https://github.com/misterblack1/appleII_deadtest). Work is in progress to be emulate all functionalities of Apple Rom Emulator Card ([050-0009-01](https://mirrors.apple2.org.za/Apple%20II%20Documentation%20Project/Interface%20Cards/ROM%20Cards/Apple%20ROM%20Emulator%20Card/Photos/Apple%20ROM%20Card%20with%20ROM%20-%20Front.jpg))
but with only one Rom chip (27128).
