+++
title="Discord bot for xkcd"
type="page"
creatordisplayname = "iuyte"
creatoremail = "iuyte@iuyte.net"
date = "2017-11-25"
+++
# <span style="color: red; font-weight: bold;">Background</span>
## <span style="color: red;">[xkcd](https://xkcd.com/)</span>
XKCD is a webcomic by [Randall Munroe](https://en.wikipedia.org/wiki/Randall_Munroe).
It consists primarily of romance, sarcasm, math, and language, appealing to a
lot of nerdy people (and some non-nerds too). I really enjoy it, and felt the
need to create a discord bot for it.

## <span style="color: red;">[Discord](https://discordapp.com/)</span>
Quote from their website as of today:

<span style="color: red; font-family: monospace;">
All-in-one voice and text chat for gamers that's free, secure,
and works on both your desktop and phone. Stop paying for TeamSpeak servers and
hassling with Skype. Simplify your life.
</span>

Additionally, it has video chat in group messages, and an API. Many libraries
have been created for a plethora of programming languages for this API. Many
people have begun to create Discord bots, that reply to messages or perform
and action based on a command, or even act as a person and try to form coherent
words, sentances and phrases.

## <span style="color: red;">The mix</span>
I use Discord daily to comminicate with people who have common interests, such
as robotics, school, programming, etc. A new xkcd comic is posted every Monday,
Wednesday, and Friday, so those are a pretty common activity for me as well.

I decided to use a Discord library for [golang](https://golang.org/) called
[discordgo](https://github.com/bwmarrin/discordgo) to do this project, becuase
I really like golang and I found discordgo to be a mature library.

## <span style="color: red;">Status</span>
The project is at a bit of a standstill right now, with crunch time for robotics
in full effect. However, I did have plenty opportunity to get it off of the
ground prior to now.
#### <span style="color: red;">What Works</span>
<ul>
	<li>Random comic - works well, fast</li>
	<li>Get comic by number - same state as random</li>
	<li>Get comic by search tag - slow</li>
	<li>Play youtube music - not necessary, but cool</li>
	<li>Search youtube for music - works, but needs more indicators of success</li>
</ul>

#### <span style="color: red;">What Doesn't</span>
<ul>
	<li>Search speed - loops over all xkcds, makes a request for each,
	selects one with most matches</li>
	<li>Events - supposed to integrate a calender, but that never really got going</li>
</ul>

## <span style="color: red;">Moving Forward</span>
Firstly, before adding any more unnecessary features, I want to fix the speed
problem. The best way to solve this would be an independent database that
updates every few minutes on each Monday, Wednesday, and Friday, until the
latest xkcd is posted. Likely, the easest way to get the latest xkcd is through
the [RSS feed](https://xkcd.com/rss.xml) or [Atom feed](https://xkcd.com/atom.xml).
