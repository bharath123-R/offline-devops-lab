<<<<<<< HEAD
By: Bharath RProject Name: B2N Dev Cloud LabPlatform: VirtualBox + Ubuntu + GitHub + Netlify

✅ Overview

This project documents the journey of building a fully offline DevOps lab using VirtualBox, Ubuntu, Git, GitHub Actions, and Apache. By Day 11, we have a working local cloud server accessible from any device in the same WiFi network.

📆 Day-by-Day Summary

🔹 Day 1 – Installed Git & VS Code

Installed Git Bash

Installed Visual Studio Code

Setup basic Git config (username, email)

Linked GitHub account using PAT


🔹 Day 2 – React App Setup

Created a Vite + Tailwind React app

Ran development server locally

Confirmed build worked



🔹 Day 3 to 5 – GitHub Sync & Netlify Setup

Created GitHub repo my-first-cloud-site

Pushed React app to GitHub

Linked GitHub to Netlify

Deployed site manually on Netlify first



🔹 Day 6 to 9 – GitHub Actions for Netlify CI/CD

Created GitHub Actions workflow YAML file

Used JamesIves/github-pages-deploy-action

Commit pushed → Netlify site auto-deploys

Debugged issues with push, auth, and Netlify token



🔹 Day 10 – VM Setup with Apache

Created VM using VirtualBox

Installed Ubuntu Server (no GUI)

Installed Apache2 with:

sudo apt update
sudo apt install apache2

Verified with:

curl http://localhost

Set up port forwarding: 8080 (host) → 80 (guest)

Accessed site from Windows via http://localhost:8080



🔹 Day 11 – LAN Access from Other Devices

Switched VirtualBox network to Bridged Adapter

Got VM IP with ip a → 192.168.1.3

Disabled UFW temporarily with sudo ufw disable

Accessed site on phone/laptop with:

http://192.168.1.3

🛠 Technologies Used

VirtualBox

Ubuntu 20.04 LTS

Apache2 Web Server

Git + GitHub

GitHub Actions CI/CD

Netlify Hosting

🚀 Skills Learned

Git & GitHub workflows

Local-to-cloud site deployment

VirtualBox networking (NAT, Bridged)

Apache hosting & port forwarding

LAN-based server access



✅ Day 12 - Vercel Deployment with SSH Key (Frontend Hosting)
🔹 What We Did:
Generated SSH Key
Command used:

bash

ssh-keygen -t ed25519 -C "bharathr1130@gmail.com"


🔸 Why?
To securely connect GitHub with our local system and push code without entering username/password every time.

Added SSH Key to GitHub

Copied public key from:

bash

cat ~/.ssh/id_ed25519.pub


Pasted into GitHub > Settings > SSH and GPG keys

Cloned the GitHub Repo using SSH
Example:

bash

git clone git@github.com:bharath123-R/vercel-react-clean.git


Deployed React App to Vercel

Connected GitHub repo to Vercel

Chose the correct repo: vercel-react-clean

Allowed auto-deploy from main branch

✅ Successfully Deployed Site:
🔗 https://vercel-react-clean.vercel.app/


📝 Day 13 — Railway Deployment (Cloud-like Server Hosting)
✅ What We Did:
Prepared React App for Deployment

Installed serve to serve the build files:



bash
npm install serve --save
Configured Railway

Connected GitHub repo

Set:


yaml
Build Command:  npm run build
Start Command:  npx serve -s build -l $PORT
Fixed Common Issues



Made sure package.json was in root

Exposed port 3000 (or 8080)

Set PORT env variable if needed

Cleared node_modules from repo for faster build

Deployment Successful ✅

App deployed

Logs confirmed app running

Link activated (after exposing port)

🌍 Why This Is Important
Unlike Vercel (which is plug-and-play), Railway simulates a real server.
You had to:

Set up commands

Serve manually

Handle ports

Debug logs

Expose service

This is the closest DevOps experience you can get as a fresher 💥

🎯 How to Explain in Interview:
"Apart from serverless platforms like Vercel, I also deployed my frontend app using Railway — which required configuring custom start commands, exposing ports, and setting environment variables. This helped me understand real-world DevOps tasks like manual hosting, port binding, and deployment debugging."
=======
# offline-devops-lab
>>>>>>> 7a52587c2643c8fe94112985650e91cd1ec8450b
