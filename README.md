# OLED-BongoCat-Revision
 
This is a revised version of other projects that create the BongoCat animations for firmware on embedded OLED screens, fixing issues and adding new features.
This project was made specifically for the Satisfaction75 Round 2 (AKA rev1), though its code can likely be stripped and repurposed for other 128x32p OLED screens.

[Reddit Post](https://www.reddit.com/r/MechanicalKeyboards/comments/svym9a/i_revised_the_bongo_cat_animation_for_the_sat75/)


<p align="center">
    <a href="https://user-images.githubusercontent.com/3449303/154800582-f79c1b5b-69fb-412d-87cc-d7c8a0e6ac1d.mp4" title="see video"><img src="output.gif" alt="Gif of the Bongo Cat Animation for the Sat75!" /></a>
</p>

## Improvements Made
- Updated code to support Satisfaction75 Round2/Rev1 firmware
- Tracked the animations directly to the user's keyboard inputs, as opposed to the original tracking to words-per-minute
- Changed the animation behavior to use a state machine between idle, prepare, and tap animation states
- Added system clock to Bongo Cat display mode
- Fixed bugs related to flickering, screen mode settings, inactivity timeouts

## Posts/Projects Used
- [Original post by u/Pop-X-](https://www.reddit.com/r/olkb/comments/h00a8b/i_made_an_oled_animation_of_bongo_cat_that/)
- [u/salvistar adaptation to 128x32p](https://www.reddit.com/r/MechanicalKeyboards/comments/nsmx2j/i_made_upopxs_bongo_cat_oled_animation_fit_on_an/) ([Github](https://github.com/nwii/oledbongocat/))
- [Satisfaction75 proof of concept by MudkipMao](https://gist.github.com/MudkipMao/7e7b75491e98c11b2e420e4520d280d7)

## How to Use
- If you plan to use this on a Satisfaction75 R2, you can simply flash the included `cannonkeys_satisfaction75_rev1_Pedker.bin` file to your board using QMK Toolbox or any other means. You can follow [this guide](https://www.youtube.com/watch?v=fuBJbdCFF0Q), but **please flash at your own risk.**
- **I am not sure if this will work for the Satisfaction75 Round1 (Rev0), so definitely flash that at your own risk.**

- Alternatively, you can include the changes made to your own firmware by either replacing the files or editing them to match the files included here
- `bongo.h`: all (new file)
- `rules.mk`: lines 26, 28, 29
- `satisfaction75.h`: lines 16, 61
- `satisfaction75_oled.c`: lines 3-5, 32-34
