🎵 Sound Bar – YouTube Audio Player (Expo + React Native)

Sound Bar ek Expo + React Native based music search application hai jisme user YouTube API ki madad se apne favorite songs search kar sakta hai aur unhe app ke andar hi play kar sakta hai.

Ye project create-expo-app se initialize kiya gaya tha aur baad me custom functionality implement ki gayi.

🚀 Features

🔎 YouTube Data API v3 se song search

⚡ Real-time search with debounce

🎬 YouTube embedded player

🎧 Audio-focused playback experience

📱 Landscape mode me fullscreen player

❌ Input clear (✕) button

⏳ Loading indicator

🎵 No results / Discover banner

🌙 Clean Dark UI

🛠 Tech Stack

Expo

React Native

react-native-youtube-iframe

YouTube Data API v3

React Hooks (useState, useEffect, useCallback)

Debounce logic using setTimeout

🔑 YouTube API Integration

App me YouTube Data API v3 use ki gayi hai.

API Endpoint Used:
https://www.googleapis.com/youtube/v3/search

Parameters:

part=snippet

q=searchQuery

type=video

maxResults=20

key=API_KEY

Implementation Flow:

User search input me text type karta hai

Debounce 500ms delay ke baad API call hoti hai

Response se:

videoId

title
extract kiya jata hai

FlatList me results show hote hain

User kisi result par click karta hai

videoId YouTubePlayer ko pass hota hai

Video play hota hai

⚡ Real-Time Search with Debounce

User jese jese type karta hai:

useEffect trigger hota hai

setTimeout (500ms) delay lagta hai

Previous timeout clear hota hai

Unnecessary multiple API calls avoid hoti hain

Isse performance improve hoti hai aur API quota save hota hai.

🎬 YouTube Player Integration

Library used:

react-native-youtube-iframe

Player Props:

videoId → selected video ID

play → playback control

onChangeState → detect video end

Landscape mode me:

Search UI hide ho jata hai

Player fullscreen height le leta hai

📱 Orientation Handling

Dimensions.addEventListener use karke:

Portrait → search + list visible

Landscape → fullscreen player mode