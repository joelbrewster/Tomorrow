# Tomorrow Theme

- Tweak colors for term vim and guivim (dark).
- Add bright colors to term so light and dark aren't identical.
- Change Tomorrow (light) to use inverted background and foreground of Tomorrow (dark).
- Match backgrounds. #262626 is the best.

![screenshot](https://i.imgur.com/HW3y4cw.png)
- Font: Fira Code 13pt

# Theme Changer
*Change for bright light situations*
- Add an alias in your bashrc, etc to change from dark to light on the fly.

`alias s="osascript ~/.vim/plugged/Tomorrow/ThemeChanger.scpt"`
- included is an app that you can load with alfred.app, launchbar, spotlight or something similar. Select the window you want to change then load the ThemeChanger.app.

- Set vim to change colors based off time.

`if strftime("%H") >= 7 && strftime("%H") < 19`
  `colorscheme Tomorrow`
  `set background=light`
`else`
  `colorscheme Tomorrow-Night`
  `set background=dark`
`endif`
