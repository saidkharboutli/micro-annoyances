# The Solutions to All My Micro Annoyances

## Background

Every so often, I run into some random problem or challenge and think: "I wish there was an easily accesible, simple web-app that solves this problem". And, to be honest, there probably is some web-app that solves that problem, but its probably a solution buried within an application that solves many other problems, and frankly I don't want to deal with that. And even if there is some easy, single-use webapp solution, its not always easily accessible. Is it ineffecient to then rewrite these solutions myself and host them on my own infrastructure so I can easily access them? Yeah. Am I gonna do it anyway, both because it makes my life easier and gives me a space to practice my web development (AI-free, minus design--I suck at that stuff)? Yes. So thats what this repository is.

## The Details

### Monorepo Structure

This mono-repo hosts several micro-projects within it. Each subfolder is its own micro-project. Each subfolder is deployed separately as its own app. Some apps will be built on JS/React (probably most), some might be Python, some might be something else entirely. The only important note is that it all gets deployed as its own webapp with Cloudflare workers. At the top level of the repository there exists a GitHub Workflows folder. These workflows cover deployment of each app by checking diff paths to selectively deploy on the apps that have changes. 

### The Infra

I love Cloudflare and they have a very generous free tier for all of their hosting services. So I am using Cloudflare. Also I don't have to worry about getting charged $100K+ because someone decides to DDoS me ([1](https://www.reddit.com/r/webdev/comments/1b14bty/netlify_just_sent_me_a_104k_bill_for_a_simple/) [2](https://www.reddit.com/r/googlecloud/comments/1jzoi8v/ddos_attack_facing_100000_bill/)). Thanks for being awesome Cloudflare. GitHub Actions for CI/CD. Workflows as explained above, so only changed projects get re-deployed. Deployments land somewhere under `apps.saidk.io`. Still deciding how I want that to look.

### The Projects

This section is a living section. I'll update this as I add more projects.

1. Test Project
