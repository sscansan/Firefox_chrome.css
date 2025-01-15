# Firefox .css tweaks

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

done!