# Firefox .css tweaks

*here my take on Morrolinux's minimal firefox* https://gist.github.com/morrolinux/87aa37396432ea5d14a9220bc4892100

## Enable Firefox features

Go to `about:config` and set all of the following to `true`:
```
    toolkit.legacyUserProfileCustomizations.stylesheets
    layers.acceleration.force-enabled
    gfx.webrender.all
    gfx.webrender.enabled
    layout.css.backdrop-filter.enabled
    svg.context-properties.content.enabled
    
    # LINUX ONLY - WORKAROUND FOR BAR HIDING ON DRAG EVENT
    widget.gtk.ignore-bogus-leave-notify = 1
```

## Write your userChrome.css

1. Find your Firefox profile folder (`about:support` --> "Profile Directory") 
2. Create a folder named `chrome` inside it.
3. Create a file named `userChrome.css` inside the `chrome` folder you just created.
4. Paste in `userChrome.css` whatever you like from above
5. Restart Firefox for changes to take effect. **If nothing changes**, try going to `about:profiles` and click the "Restart Normally" button in the upper right portion of the screen. Thanks @kr1s7ian for pointing this out.

## To hide the "classic" horizontal tab toolar entirely

Paste the content of `userChrome.css` in your local chrome/userChrome.css

And then go to `Sidebery settings` > `General` > `Preface value`, enable it and set it to `XXX`.

Now You also need to remove indent when the bar is collapsed, or you won't be able to see all tabs

Go to `SideBery settings` --> `Styles editor` and add:

```
#root:not(:hover){
  --tabs-indent: 0;
}
```

done!
