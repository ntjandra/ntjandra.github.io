---
layout: post
title: Website Footer Redesign
date: 2024-02-16 5:30 -0700
tags: memo trial pin
---

Another new year brings a ton of new innovation, especially in the realm of AI. Found a new cool AI tool called Locofy, so I'm trying it out to redo my website footer.

## Tools of the trade

To begin my journey of a major website revamp/overhaul, I had plenty of ideas inside my head. But it's easier to view outside of my head, so I learned Figma and spent time looking at templates. I also took the time to work on frontend layouts during my spare time since I was making a digital character sheet for ActiveRPG. Grids and Boxes don't always go where I think they go, so I stuck with row/col for this one.

### Figma

I've been learning Figma to improve the layout and organization to bring to life what I picture as the website. I'm nowhere near the level of a UI designer like the one I worked with at Mage, but I know how to move components and the general tree layout of frames.

### Locofy

Wanting to check off some items from my bucket list, I knew I wanted to visit/live in South East Asia for a while. I browsed for LinkedIn jobs in Singapore and saw a Developer Advocate position at a company called Locofy. I took a look at the product, joined their Discord server and introduced myself. They were pretty quick when responding despte the timezone difference, so the next day I signed up for the product on a 21 day trial.

I didn't feel confident enough to apply to the job posting though. As part of their beta account sign up process, I did have to post my portfolio site, so there's a chance they'll come across this post.

Ok enough rambling, Locofy is a neat AI software that transforms Figma Designs into frontend code. For my footer, I'm using it to generate basic HTML/CSS since I use GitHub pages for free domain hosting as long as it's Jekyll content.

## My experience

I built a new footer in only a day, which is certainly a major improvement from my old footer. Locofy was great at getting the basic css looks that I desired, then it was back to me to rewrite my css and integrate the generated code with my components.

### Getting started

The new footer was built after sifting through design templates of Footers on Figma and slowly piecing together the parts I liked the most. Once I created a design I'd run the Locofy plugin and get a decent preview. There I could manually make some slight edits such as the frame groupings. I grouped based on waht fit best for the html nesting.

The ideal template I had created featured 3 sections: Profile, Navigation, and Search. I reused most of my old code for the profile section and used Figma to align the dividers in a cleaner and less packed format. For navigation, I knew because I didn't have navigation in the header (sidebar only), visitors might not find how to navigate.

Using the Locofy Plugin and getting the right results were two different matters though. In my inital stages, I tried to do edits in code but later realized in future generations it wouldn't detect code changes because it scans a Figma file. It's currently one-way not two-way so that meant I had to "code in Figma".

### Squashing bugs

Once I had the footer design flushed out, I'd export it to my computer and toss it into the .html and .css files for my footer. This obviously isn't magical and I spent most of the time integrating in the code and squashing bugs.

I spent a lot of time on integration, way more than my Figma design. A common issue I ran into is that most designs have a common component, which would overlap or overide my own because of the order I imported the .css file. In this case, it was the button. I noticed it broke my next post styles on the blog page and applied a bandaid fix by making the class less generic.

Another example is links, the design scanner didn't detect links and I didn't want to write a link overide for only the color, so I had to adjust my original color themes to match what I wanted. I really wanted to get a nice blue footer, but it matches the link color a bit too closely. Changing the link color would also change my tags, so I gave in and went with the original green the site used to be.

Finally, there was readibility. My feelings as a former SDE and now Technical writer meant I took it personally when the names generated were wacky. Most Figma design components are called frames and the ai generated names would be in k-e-b-a-b style. I did my best to clean up the classes with some find and replace.

## Satisfaction

I am proud and impressed by what I was able to create. Admittedly, I've proctastinated hard on getting this site updated. I'll continue to see what other design layouts I can try before my trial period ends. I do feel bad about the resource usage I incurred as I scanned the same frame so many times.

### Room for improvement

I included in my design the [AIMe Search](/2023-05-25-AI-Me.md) component I was working on, however my Semantic Reactor project only works in Spreadsheet so far. It isn't understanding the instructions when I pass it in as a script and the fine-tuning instructions also break. After this footer, what's next is my post timeline. It'll be much larger in scale since I'm scrapping the old timeline completely.
