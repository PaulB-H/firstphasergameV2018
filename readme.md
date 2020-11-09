# First Phaser Game version 2018

<b>Post-Completion Additions:</b><br>
Added loading screen using following guide:<br>
[Create loading screen in Phaser 3](https://gamedevacademy.org/creating-a-preloading-screen-in-phaser-3/)<br>
<br>
Project now loads an example image 500 times in order to show the loading bar for long enough, else assets are so small game loads instantly and you never see loading screen

<hr>

Following the official first game tutorial from Phaser<br>
[Link](https://phaser.io/tutorials/making-your-first-phaser-3-game/part1)<br>
<br>
This guide uses some older practices such as var instead of let. The next project is a 2020 version of this same project and will use modern practices

## Methods and Docs

Config<br>
[GameConfig Object](https://photonstorm.github.io/phaser3-docs/Phaser.Types.Core.html#.GameConfig)
<br>
Game<br>
[Game Instance](https://photonstorm.github.io/phaser3-docs/Phaser.Game.html)<br>
<br>
[Phaser.Physics.Arcade.Sprite](https://photonstorm.github.io/phaser3-docs/Phaser.Physics.Arcade.Sprite.html)

Creating player sprite

    player = this.physics.add.sprite(100, 450, "dude");

#### Issue tracker:

<hr>
Assets not loading<br>
Fix: Move static files to public folder, change how assets are called

    function preload() {
        this.load.setBaseURL("assets");
        this.load.image("sky", "sky.png");
        ....
    }

    // server.js
    app.use(express.static("public"));

<hr>
