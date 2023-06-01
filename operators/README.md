![](../images/line3.png)

### Blueprint Operators

<sub>[previous](../text/README.md#user-content-names-strings-text) • [home](../README.md#user-content-ue5-bp-overview) • [next](../)</sub>

![](../images/line3.png)

Lets create a countdown timer and see how we use operators which is a bit different in Blueprints compared to doing it in C++.

<br>

---

##### `Step 1.`\|`BPOVR`|:small_blue_diamond:

Select the **Blueprints** folder and right-click in the open folder and select an **Blueprint Class** and select **Actor**.  Call the new blueprint `BP_Countdown`.

![create BP_Countdown](images/countdownBP.png)

![](../images/line2.png)

##### `Step 2.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: 

Open up **BP_Countdown** and add a **Text Render** component.  Chnage the name to `CountdownTimer`.  Copy and paste the **Text Render Color** so it is the same as the others. Change the **Horizontal Alignment** and **Vertical Alignment** to `Center` and `TextCenter`. Change the **Text** to `Countdown Timer` and the **World Size** to `72`.

![add CountdownTimer component and format text](images/countdownTimerComponent.png)

![](../images/line2.png)

##### `Step 3.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

This time we will not use the **Begin Play** but instead use the **Tick Event**.  In Unreal Engine, a **Tick Event** refers to a specific type of event that occurs every frame or at a regular interval. It is commonly used to update and control the behavior of objects or actors within the game world.

Think of the game world as a continuous flow of time, divided into small increments called frames. Each frame represents a snapshot of the game's current state, including the positions and properties of all objects. 

During each frame, the engine goes through various processes, such as rendering graphics and handling player input. In addition, it triggers tick events for objects that have been set up to receive them.

When an object receives a tick event, it means that the engine is giving it an opportunity to perform some actions or calculations. For example, an enemy character might use the tick event to update its position, check for collisions with other objects, or react to player input.

The tick event is called repeatedly, typically 30 or 60 times per second, depending on the frame rate of the game. This regular repetition ensures that objects can constantly update and respond to changes in the game world, providing smooth and interactive gameplay.

By utilizing the tick event, game developers can create dynamic and responsive behaviors for objects in Unreal Engine, making the game world come alive with movement and interactivity.

Drag the **Countdown Timer** to the graph and drag off the pin and add a **Set Text** node.  Now we will take the **Delta Seconds** pin and send it to the **Set Text | Value** pin.

![set text with delta time](images/deltaSecondsEventTick.png)

![](../images/line2.png)

##### `Step 4.`\|`BPOVR`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 5.`\|`BPOVR`| :small_orange_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 6.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 7.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 8.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 9.`\|`BPOVR`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 10.`\|`BPOVR`| :large_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 11.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 12.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 13.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 14.`\|`BPOVR`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 15.`\|`BPOVR`| :large_blue_diamond: :small_orange_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 16.`\|`BPOVR`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 17.`\|`BPOVR`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 18.`\|`BPOVR`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 19.`\|`BPOVR`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 20.`\|`BPOVR`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 21.`\|`BPOVR`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT PAGE"> -->

![next up - ](images/banner.png)

![](../images/line.png)

| [previous](../text/README.md#user-content-names-strings-text)| [home](../README.md#user-content-ue5-bp-overview) | [next](../)|
|---|---|---|