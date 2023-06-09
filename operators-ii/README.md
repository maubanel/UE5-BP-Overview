![](../images/line3.png)

### Blueprint Operators II

<sub>[previous](../operators/README.md#user-content-blueprint-operators) • [home](../README.md#user-content-ue5-bp-overview) • [next](../iteration/README.md#user-content-blueprint-iteration)</sub>

![](../images/line3.png)

Now that we have the countdown working, lets add the ability to reset it back to `10` when you press the <kbd>R</kbd> key.

<br>

---

##### `Step 1.`\|`BPOVR`|:small_blue_diamond:

Open up **BP_Countdown** and press the **+ Add** button to add another **TextRender** component.  Rename it to `Reset Counter`. Make it a different **Text Render Color** and **World Size** of `26`.  Change the **Horizontal Alignment** and **Vertical Alignment** to `Center` and `Text Center`.  Change the **Text** to `Press R to Restart Countdown`.

![add reset counter textrender component](images/addResetNode.png)

![](../images/line2.png)

##### `Step 2.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: 

Press the <kbd>Play</kbd> button and you will see that the message is visible the entire time. We want it to start without this message.

![reset title appears when you hit play](images/alwaysReset.png)

![](../images/line2.png)

##### `Step 3.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Drag a **ResetCounter** reference to the graph.  Also right click on the empty graph and add a **Event Begin Play** node. Drag off of the **ResetCounter** pin and select **Set Hidden in Game** node.

![being playe hiddent in game](images/setHidden.png)

![](../images/line2.png)

##### `Step 4.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Connect the execution pin from **Begin Play** to **Set Hidden in Game** then make sure **New Hidden** is set to `true`.  This ensures the object does not render in game.

![set reset counter hidden in game](images/newHiddenTrue.png)

![](../images/line2.png)

##### `Step 5.`\|`BPOVR`| :small_orange_diamond:

Now that we turned it off, we want to turn it on when **Game Time** is les than `0`.  So intercept the execution pin coming out of **Set GameTime** to `0` and add a reference to **ResetCounter** and and pull off the pin to add another **Set Hidden in Game** node, but this time set the **New Hidden** to `false` showing the text.

![turn instruction text on when 0](images/Unhide.png)

![](../images/line2.png)

##### `Step 6.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond:

Press the <kbd>Play</kbd> button and when the timer gets to `0` the message appears.

https://github.com/maubanel/UE5-BP-Overview/assets/5504953/64cacc97-f10d-46a7-8995-2a20efed8daf

![](../images/line2.png)

##### `Step 7.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now we need to reset the timer when `R` is pressed. Add a **Keyboard R** event.

![add keyboard r event](images/addREvent.png)

![](../images/line2.png)

##### `Step 8.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now we do not want to do anything unless the reset counter is visible.  So drag a reset counter reference to the graph and pull of the pin and add a **Is Visible** node which will return `true` if it is visible in the game.

![alt_text](images/whenResetVisible.png)

![](../images/line2.png)

##### `Step 9.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Then add a **Branch** node and when `true` add a **Set GameTime** variable nad reset it to `10`. Select all the nodes going to the **Event R** and press the <kbd>C</kbd> key and add a `Reset Timer` heading to the comment box and give it an appropriate color.

![reset game time to 10](images/branchComment.png)

![](../images/line2.png)

##### `Step 10.`\|`BPOVR`| :large_blue_diamond:

Go to the top component in the blueprint and make sure the blueprint can receive input by setting **Input | Auto Receive Input** to `Player 0`.

![set auto receive input to Player0](images/absorbInput.jpg)

![](../images/line2.png)

##### `Step 11.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: 

Press the <kbd>Play</kbd> button and when you cannot reset the timer until it gets to `0`.  That is working.  But once you do reset the time, the reset timer text is still showing.

https://github.com/maubanel/UE5-BP-Overview/assets/5504953/b50ff055-f77e-4229-8e4d-d543cd2df8cd

![](../images/line2.png)

##### `Step 12.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Turn **Reset Counter** text back to **Hidden** after **GameTime** is reset.

![alt_text](images/setHiddenAfterReset.png)

![](../images/line2.png)

##### `Step 13.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Press the <kbd>Play</kbd> button and now we have a reseting timer working correctly with all known edge cases addressed.  Congrats!

https://github.com/maubanel/UE5-BP-Overview/assets/5504953/590b5d73-aeab-4f82-9640-a0a39e123421

![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - Iteration"> -->

![next up - ](images/banner.png)

![](../images/line.png)

| [previous](../operators/README.md#user-content-blueprint-operators)| [home](../README.md#user-content-ue5-bp-overview) | [next](../iteration/README.md#user-content-blueprint-iteration)|
|---|---|---|
