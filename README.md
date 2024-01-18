<div align="center"><img  height="150px" src="https://i.imgur.com/0lfS9gN.png" /></div>
<h1 align="center"> PenQuiz </h1>

PenQuiz is a trivia PvP game which is set in Antarctica. Game offers multiple playable characters with various abilities that help the player throughout the game. The game consists of 3 different stages with multiple rounds and requires 3 people per match to play. Capture territories from other players with engaging trivia questions. Scoring is based on the amount of territories and points you own.
<br />
<br />
This repository contains documentation and information regarding the PenQuiz project.

# Table of contents
1. [Source](#source)
2. [Features](#features)
3. [How to play?](#production)
4. [Game rules](#gamerules)
5. [Game characters](#gamecharacters)
6. [Architecture](#architecture)
7. [Backend stack](#backendstack)
8. [Frontend stack](#frontendstack)
9. [In game pictures](#ingamepictures)

# Source <a name="source" />
- Backend repo - https://github.com/BoostedPenguin/PenQuiz-Backend
- Frontend repo - https://github.com/BoostedPenguin/PenQuiz-Frontend

# Features <a name="features" />
- Engaging trivia battles
- Multiple playable characters
- Public matchmaking
- Private lobbies
- Game bots
- Match history and statistics
- Submit your own questions to the game
- Login with Google account
- Admin panel

# How to play? <a name="production" />
Visit https://penquiz.netlify.app/ and create a free to play account.

For android devices please download the app and install it from <a href="https://onedrive.live.com/download?cid=D25E3AABFBD442D5&resid=d25e3aabfbd442d5%2112006&authkey=AFUTx5Dgm91DciU">here.</a> 

# Game rules <a name="gamerules" />

<img src="https://i.imgur.com/SiB9DFV.png" />


# Game characters <a name="gamecharacters" />
<img src="https://i.imgur.com/wpWDyhZ.png" />

Currently there are 4 playable characters in PenQuiz. Most of the characters are free to play, however some are premium and require to be purchased first before the user has the option to play them. Each champion has different in-game abilities.

## Wizard
Can remove 2 of the wrong answers in a multiple choice question. Ability can be used total of 3 times per game.

## Scientist
Can narrow down the number choice question answer. Ability can be used 3 times per game.

## Viking
Can fortify his capital against attacks, increasing the amount of required consecutive wins for the enemy. Ability can be used a total of 2 times per game.

## King
Has a permanent 10% score bonus multiplier when you capture a territory (Premium character)


# Architecture <a name="architecture" />
The backend consists of 3 microservices which utilize RabbitMQ and GRPC to communicate with each other and send messages via SignalR to the frontend React Native application.

<img src="https://i.imgur.com/kaaqNMW.png" />

# Backend stack: <a name="backendstack" />
* NET 6
* SQL Server / PostgreSQL (Entity ORM)
* CockroachDB
* SignalR
* GRPC
* JWT Authentication
* RabbitMQ
* Docker
* Kubernetes
* Azure App Services

# Frontend stack: <a name="frontendstack" />
* React Native
* Expo SDK 44
* SignalR Client
* JWT Authentication
* Google auth
* Native-base
* Netlify

## Communication between Microservices <a name="microservicescommunication" />
Embracing eventual consistency pattern, we use the RabbitMQ message bus to send messages between the microservices and we "pull" for any missing data whenever a microservice starts.

<img src="https://i.imgur.com/kO8WVuO.png" />

# In game pictures <a name="ingamepictures" />

## Game map screen
<img src="https://i.imgur.com/fJgJbfM.png" />

## Dashboard screen
<img src="https://i.imgur.com/iwqTmW2.png" />

## Character screen in lobby
<img src="https://i.imgur.com/Y2jUmr1.png" />

## Game lobby screen
<img src="https://i.imgur.com/GjURWu3.png" />

## Login screen
<img src="https://i.imgur.com/u8NRHgS.png" />

