# First Phaser Game version 2018

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
