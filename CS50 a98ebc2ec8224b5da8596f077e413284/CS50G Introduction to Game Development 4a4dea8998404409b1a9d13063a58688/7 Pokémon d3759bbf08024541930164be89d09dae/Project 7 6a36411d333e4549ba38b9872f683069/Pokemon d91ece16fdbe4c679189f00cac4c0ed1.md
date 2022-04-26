# Pokemon

## **Objectives**

- Read and understand all of the Pokémon source code from Lecture 7.
- Implement a `Menu` that appears during the player Pokémon’s level up that shows, for each stat, ‘X + Y = Z’, where X is the starting stat, Y is the amount it’s increased for this level, and Z is the resultant sum. This `Menu` should appear right after the “Level Up” dialogue that appears at the end of a victory where the player has indeed leveled up.

## **Demo**

*by Edward Kang*

[https://youtu.be/E8QML69Zww0](https://youtu.be/E8QML69Zww0)

## **Getting Started**

Download the distro code for your game from [cdn.cs50.net/games/2018/x/projects/7/pokemon.zip](https://cdn.cs50.net/games/2018/x/projects/7/pokemon.zip) and unzip `pokemon.zip`, which should yield a directory called `pokemon`.

Then, in a terminal window (located in `/Applications/Utilities` on Mac or by typing `cmd` in the Windows task bar), move to the directory where you extracted `pokemon` (recall that the `cd` command can change your current directory), and run

`cd pokemon`

## **Next-Level**

Welcome to your eighth assignment! This week’s code will probably be the most complicated we’ll look at during the semester, but the assignment itself is fairly small in comparison; you will, however, need to know how many of the pieces work and fit together in order to accomplish the task ahead.

## **Specification**

- *Implement a `Menu` that appears during the player Pokémon’s level up that shows, for each stat, ‘X + Y = Z’, where X is the starting stat, Y is the amount it’s increased for this level, and Z is the resultant sum. This `Menu` should appear right after the “Level Up” dialogue that appears at the end of a victory where the player has indeed leveled up.* The area where most of this will take place is the `TakeTurnState`, specifically in the `:victory()` function, where the actual detection of a level up takes place. Ordinarily, just a `BattleMessageState` gets pushed onto the `StateStack`, but we’ll need to go a step further and push an additional `Menu` in order to accomplish what we’re after. This `Menu` should not have a cursor like the other `Menu` we’re used to seeing (in the `BattleMenuState`!), so you’ll need to customize the `Selection` class a little bit in order to take a boolean value to turn the cursor on or off as needed (defaulting to `true` if needed to preserve the behavior of the `Menu` in the `BattleMenuState`). Note that the `:levelUp()` function in the `Pokemon` class returns all of the stat increases we need in order to display things properly, so be sure to use those returned values when creating the `Menu`! As long as you get a proper grasp on the `Selection`, `Menu`, and `StateStack` classes, this assignment should be relatively straightforward in comparison to the complexity of this week’s code as a whole!

## **How to Submit**

When you submit your project, the contents of your `games50/projects/2018/x/pokemon` branch must match the file structure of the unzipped distribution code exactly as originally received. That is to say, your files should not be nested inside of any other directories of your own creation or otherwise deviate from the file structure we gave you. Your branch should also not contain any code from any other projects, only this one. Failure to adhere to this file structure will likely result in your submission being rejected.

By way of a simple example, for this project that means that if the grading staff visits `https://github.com/me50/USERNAME/blob/games50/projects/2018/x/pokemon/src/states/game/TakeTurnState.lua` (where `USERNAME` is your own GitHub username as provided in the form, below) we should be brought to the `TakeTurnState.lua` file for 50-Mon. If that’s not how your code is organized when you check (e.g., you get a 404 error or don’t see your edits), reorganize your repository as needed to match this paradigm.

1. If you haven’t done so already, visit [this link](https://submit.cs50.io/invites/46e6f2ea29954ce9bb1bdc478a440055), log in with your GitHub account, and click **Authorize cs50**. Then, check the box indicating that you’d like to grant course staff access to your submissions, and click **Join course**.

The change to `/projects/2018` below is intentional, as CS50 courses have changed to a scheme that reflects when the project was initially released. So the 2018 here is correct, even though it’s no longer 2018! Also note that the **video** for this project is optional, you do not need to complete it if you do not want to. This is only true for this project, Project 0, and Project 6. For all other projects, a video is mandatory.

1. Using [Git](https://git-scm.com/downloads), push your work to `https://github.com/me50/USERNAME.git`, where `USERNAME` is your GitHub username, on a branch called `games50/projects/2018/x/pokemon` or, if you’ve installed `[submit50](https://cs50.readthedocs.io/submit50/)`, execute
    
    `submit50 games50/projects/2018/x/pokemon`
    
    instead.
    
2. [Record a screencast (if you want)](https://www.howtogeek.com/205742/how-to-record-your-windows-mac-linux-android-or-ios-screen/), not to exceed 5 minutes in length, in which you demonstrate your app’s functionality. [Upload that video to YouTube](https://www.youtube.com/upload) (as unlisted or public, but not private) or somewhere else.
3. [Submit this form](https://forms.cs50.io/e827348d-1802-43a0-a070-67db983ec21d).

You can then go to [https://cs50.me/cs50g](https://cs50.me/cs50g) to view your current progress!