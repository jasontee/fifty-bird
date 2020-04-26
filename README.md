# fifty-bird

This repo is forked from games50/fifty-bird.

In push.lua, love.window.getPixelScale has been replaced with love.window.getDPIScale (https://love2d.org/wiki/love.window.getPixelScale) because getPixelScale has been renamed.

The assignment requires the following:
1. Random gaps between pipes.
2. Random intervals between pipes.
3. Show a medal to congratulate the player for a high score.
4. A pause mechanism.

Solutions:
1. In PipePair.lua, the lower pipe is set to be drawn at PIPE_HEIGHT + a random of math.random(80, 120), given a y point.
2. In PlayState.lua, the next pipe is set to be drawn after math.random(2, 25) seconds.
3. In ScoreState.lua, if the player scores at least 3 points when game is over, a medal and a congratulatory message is shown.
4. In PlayState.lua, a self.pause variable is created as a switch to pause the game when player presses 'p'.
