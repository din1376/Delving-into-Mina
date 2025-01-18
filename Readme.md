# Crafting Your First zkApp on Mina

In the mystical lands of blockchain, where privacy is more precious than a golden ticket to Willy Wonka's factory, there lies a protocol known as Mina. Powered by the enigmatic magic of zero-knowledge proofs (zk-SNARKs), Mina boasts a blockchain that's lighter than your ex's commitment issues. Here, we're not just building apps; we're crafting **zkApps** smart contracts with a penchant for privacy and a disdain for high gas fees.


![mina1-modified](https://github.com/user-attachments/assets/42d36f97-48e7-44a1-a201-937ce0b360f4)

## The Quest Begins: Understanding Mina's Magic

Imagine a blockchain where transactions are faster than your last relationship ended, and the gas fees are as flat as the Earth in a flat-earther's dream. This is the world of Mina, where off-chain computations mean you're only paying for the proof, not the process. 



## Prerequisites for the Journey:

- **zkApp CLI**: Your magical wand for this adventure.  
- **TypeScript**: Because JavaScript needed to grow up.  
- **Node.js (v18+), npm (v10+), git (v2+)**: The basic toolkit of any modern mage.  

> *Pro Tip*: Don't forget to reload your terminal post-installation; we don't want any magic spells misfiring!


## The Two Paths: o1js or Protokit?
![mina2-modified](https://github.com/user-attachments/assets/b58e3bbb-0b5f-436b-956a-5b91741dde77)
---
## **o1js - The Beginner's Elixir**

![mina0-modified](https://github.com/user-attachments/assets/ef34c816-5ce8-46dc-b3f9-63f05f333a5e)


o1js is like the friendly wizard who teaches you the ropes. It's TypeScript-based, making it as comforting as your favorite blanket. Here's how you start:

```bash
npm install -g zkapp-cli
zk --version  # Check if your wand is ready
zk project your-magical-project-name  # Create your spellbook (project)
```

#### Building with o1js:
1. **Install**: Get your CLI wand ready.  
2. **Create**: Summon your project with a simple incantation.  
3. **Navigate**: `cd` into your new magical land.  
4. **Test & Build**:  
   ```bash
   npm run test
   npm run build
   npm run start
   ```
5. **Deploy**: Configure, fund, and cast your zkApp into the wild with `zk config` and `zk deploy`.

#### Use Cases:
From sudoku puzzles to tic-tac-toe, o1js is your playground for general-purpose zk circuits.

#### When to Use o1js:
If your project's state management fits within **eight on-chain field elements**, you're in the right place. Otherwise, you might need the experimental Offchain Storage API, like needing a bigger backpack for your adventure.


---
## **Protokit - The Advanced Sorcerer’s Choice**
![mina3-modified](https://github.com/user-attachments/assets/53471822-5880-46e2-8ff2-4abdbb44deba)

For those who've danced with Solidity, Protokit feels like coming home to a familiar spellbook but with privacy spells. It’s perfect if:

- Your project needs to handle more load than a Black Friday server.  
- You require access to shared or global state like a true blockchain hero.  
- You're already versed in the Ethereum scrolls.  

#### Building with Protokit:
1. **Clone the Starter Kit**:  
   ```bash
   git clone https://github.com/proto-kit/starter-kit my-chain
   cd my-chain
   nvm use
   pnpm install
   ```
2. **Test Your Spells**:  
   ```bash
   pnpm run test --filter=chain
   ```
3. **Launch Your Chain**:  
   ```bash
   pnpm env:inmemory dev --filter chain  # Sequencer
   pnpm env:inmemory dev --filter web  # UI
   ```
4. **Interact with Magic**: Open `localhost:3000`, set up your Auro wallet (the blockchain equivalent of a magic wand), and claim your tokens like a true adventurer.



## A Word on Security - Don't Get Your Scroll Hacked

In this realm, security is not just about locking your door; it's about not trusting anyone, not even the caller of your zkApp method. Here's the wisdom from the Mina council:

- Keep your logic within the proof; don't let it wander.  
- Don't trick o1js; it's smarter than you think.  
- Never trust anyone; assume they're all potential dark wizards.



## The Grand Finale

And there you have it, from the depths of TypeScript to the heights of privacy-focused blockchain applications. You've now walked through the creation of a zkApp on Mina, choosing between the comforting embrace of o1js or the powerful, interoperable magic of Protokit. Whether you're here for the privacy, the performance, or just to say you've tamed a blockchain, remember: in the world of zkApps, **your data's privacy is your dragon to protect**.

So go forth, coder, and may your zkApps be as secure as a Gringotts vault and as private as the Hogwarts' Marauder's Map!
