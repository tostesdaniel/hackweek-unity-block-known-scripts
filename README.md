# My Hackweek for Facepunch and Rust

Well, since I don't access to the official hackweek I made my own. So here the history:

## The issue

Rust is getting a lot of cheaters recently, at least since the change of the recoil in june/2022. This is on going problem and is increasing a lot, and I know facepunch is trying to fix this cat/mouse chasing issue. Yet another problem has been raising for more than 6 years now.

- **Scripting**

## The denial

For the casual player, this isn't a main threat, because they play on a 200 pop max or modded servers. This servers the fights aren't the actual goal but to have fun, learn game mechanics or play with friends. Every time someone talks about scripts and recoil control, this players don't see this as an issue and believe this isn't a "real" problem.

On the other hand, when you play on a high pop or very competitive servers it isn't hard to find a gun play where you think something isn't right about the way you died. Checking the combatlog and find out you got hit 6 times in the leg over ~~150meter~~ 200 meters (Jake Rich Correction) , makes you wonder how this guy has a such great precision with the Assault Rifle ('AK47'). If this guy was a cheater, you would have probably died with multiple hits on the head. If he isn't cheating, am I just Bad at the game? The actual reality is that he might be a scripter.

## The actual situation

Today when you join a competitive clan, they ask if you use some sort of cheat, but ignore completly if you use scripts to control recoil. They do this because hacks are actually bannable, but scripting is so hard to detect by EAC or the server Admins, that clan owners even encourage to use it.

This clan behaviour is due to other clans using the same tactic.

- Clan owners might encorage members to use some recoil control scripts to improve the odds of winning a fight.

This isn't a just clan situation. When you play with a group for some time, they disclosure their tactics for you and you realize that they are scripting for a while now. This gives a sensation of security to use external tools to improve "artificially" yourself, convincing yourself that scripting is OK.

## Not a New problem

On old Rust, legacy Rust, the problem with cheaters before EAC was beyond a simple problem, it was obnoxious. After EAC and a lot of ban waves, Rust was good again until the Auto Hot key Era.

The first scripting method used was AHK ( auto hot key ), a simple program that was easy to setup for the very old recoil on the AK. After that began the Bloody/A4 mouse, that facepunch had to make a detection and disable the core of the mouse periodically. Which solved the problem for sometime, in my opinion this was the BEST time to play Rust and thats why so much people say this was the best time to play it. Not because of the old recoil or the skill gap that was in between players that actually trained on UKN, but because there was a period of 1 year that their was zero to none scripters in the game.

After Bloody mouse era, the main scripting platform is Logitech G HUB. Just as simple as CTRL+C CTRL+V and you now have a working script, that your bad influnce friend gave to you.

## The answer

This "hackweek" I tried to solve this issue with a simple solution, trying to map and detect if the player is using a script to control recoil. By using a API to receive all the scripts detected in the player's machine, we can manually analyze each one. This way if a player has a script that is already know by database as a script to control recoil, YOU Facepunch can kick from the server like Bloody mouse is now or even better make a Ban wave with this data and give us players another YEAR of the best game in the Steam.

## Detecting so far

- ✅ Logitech GHUB
- ✅ Razer Synapse
- ✅ Red Dragon
- ❌ Corsair Icue
- ❌ Bloody Mouse
- ❌ HyperX

## Instructions

### Prerequisites

- Node.js 20+

### Quick start

1. Clone the repository:

   ```bash
   git clone git@github.com:regisdetoni89hackweek-unity-block-known-scripts.git

   cd hackweek-unity-block-known-scripts
   ```

2. Setup the environment

   _In the repository root run:_

   ```bash
   npm install

   npm run setup
   ```

3. Setup the environment variables:

   - On `block-scripts-api` folder, copy the `.env.example` to `.env` and fill the variables.
   - On `block-scripts-frontend` folder, copy the `.env.example` to `.env.local` and fill the variables.

4. Start development server:

   ```bash
   npm run dev
   ```

5. Open [localhost:3000](http://localhost:3000)

## Future Implementations

- 💡Text Analyzer to prioritize scripts to check
- ✅ Interface to flag scripts as safe or malicious
