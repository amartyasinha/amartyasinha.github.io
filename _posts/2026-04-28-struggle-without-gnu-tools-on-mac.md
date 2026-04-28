# The struggle without GNU Tools on macOS is real

The only reason I prefer MacBooks over other laptops is the build quality, force touch trackpad, and power efficiency due to arm chips. But it comes with a major tradeoff: I'm tied to macOS instead of Linux distros (yes, I know about Asahi Linux, but that's another story). Though I don't hate macOS, in fact, I like a few native features such as Spaces (multiple desktop) and Spotlight search. But let's not forget the struggles we face on macOS due to the lack of GNU tools.

I first hit this wall about a year and a half ago during a technical interview. I had to perform a task which involved sed and grep, and I showned up with my MacBook, assuming my standard Linux based workflow would carry over. I had no idea that macOS's version of these tools bahaves differently until the script failed mid task. I ended up scrambling through man pages to find the correct flags. That day, I learned a hard lesson that macOS uses BSD utilities by default instead of the GNU counterparts I was used to.

Moving forward, now that I use macOS for work, it's a pain to use BSD utilities, specially with existing projects. I run a make target, and it fail because the functionality of BSD sed is different a bit. After enough frustration, I finally started to make GNU utilities the default on my system.

Shoutout to @skyzyx for creating [this doc](https://gist.github.com/skyzyx/3438280b18e4f7c490db8a2a2ca0b9da) and @abouteiller for [this comment](https://gist.github.com/skyzyx/3438280b18e4f7c490db8a2a2ca0b9da?permalink_comment_id=3049694#gistcomment-3049694). They saved me from banging my head against the wall while configuring these tools. Embracing the developer mantra of "why do it manually once when you can spend hours automating it", I created a [bash script](https://github.com/amartyasinha/dotfiles/blob/main/scripts/setup-gnu-tools.sh) to automate these two steps.

I won't need to use this script often, but when I upgrade my Mac in the future, I can just run this script and forget the struggle of using BSD utilitis on mac.
