# Progress bar vault launch
```css
/* Vault launch progress bar change color */
.progress-bar-subline {
  position: absolute;
  background-color: var(--base2);
  height: 8px;
}

.progress-bar-line {
  position: absolute;
  opacity: 0.4;
  background-color: var(--base2);
  width: 150%;
  height: 8px;
}
```

Alternatively use this [Obsidian forum](https://forum.obsidian.md/t/progress-bar/9092/3)
```css
/* in `.theme` put: */
--interactive-accent: var(--base2)
```

Comment by “Cannibalox” (Obsidian forum) on progress bar:

> to inspect elements like this (elements that appear on specific events like hover, timer, etc) : use the PAUSE function of the devtools (f_ or CTRL ) : . open obsdian's devtools with CTRL SHIFT I or F12 . go to the `sources` tab, there is a play/pause icon in the sub-header menu . on obsidian, trigger your event (ie: hover over a link to see the popup or in your previous case, refresh Obsi with `CTRL R` to see the loading bar)
>
> while the event is active, hit F8 or CTRL / to pause obsidian (it will 'freeze' obsi until you hit F8 again)
>
> now, in devtools, switch to the `elements` tab and inspect the event as you normally would . tweak and copy your modified parameters . once you're done inspecting the css, hit F8 or CTRL \ to un-pause
>
> you can google `devtools + pause` for more infos on the process. it's easier to do than to describe really

Comment by PB:

> Klaas:
>
> The problem is the next step after finding the element that needs to be addressed is knowing the syntax that achieves what you're after.

Answer from Cannibalox:

> the devtools should provide suggestions, when you inspect to find the css corresponding to the elements, in the `styles` tab you can tweak values in real time. if you delete a value, it should provide suggestions / autocompletion. Then you copy the rule to your obsidian css. you can use https://www.w3schools.com/css to find relevant infos when you need something specific like taxonomy / syntax / commands
