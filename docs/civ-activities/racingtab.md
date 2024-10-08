---
title: Racing Tablet
parent: Civ Activities
nav_order: 5
---

## Racing Tablet

📷 [Images & Video](#Preview) 📺

**Features:**
- [Create tracks](#track-creation)
- Host races
- Buy-Ins
- [Automated Races](#Automated-Races)
- Phasing/Ghosting
- Reversed tracks
- Participation payouts
- Elmination races
- [Racing user system with customizeable auth](#user-management)
- ELO system for ranked racing
- Crew system with rankings
- Elmination Races
- Advanced leaderboards
- [Customizeable checkpoints](#gps-settings)
- Race positions
- [Curated tracks](#track-curation) (mark tracks as verified good)
- Split times
- Translateable
- [Track Sharing](#track-sharing)
- Optional default tracks
- Forced first person mode
- Vehicle Performance Class limits
- Support for Renewed Crypto

# Racing App

### GPS settings
At the bottom left corner there's a cog wheel. Clicking this brings up the options menu (more stuff to come). But here you can toggle using the GPS route and the style of it.

### Track Curation
Our idea with this feature is to allow admins to flag a track as "DONE". The track can no longer be edited. Additional features of curated tracks might be only allowing participation money to be paid out on those tracks, for example.

### Track Creation
The key to this script working is making tracks that works well. If you're trying to do 200 checkpoint style races with checkpoints randomly thrown around the map, this is not the script for you. There is a max checkpoint variable in the config that will warn users when they reached the level. Some PCs might struggle with different lower/higher amounts tho, so keep that in mind.

- Avoid placing checkpoints on/under/near bridges/overpasses. 
- GTA GPS can't handle opposite-directions on roads: Place checkpoints on the correct side of the road
- Intersections can be tricky for the GPS. We advice to not put checkpoints in the middle of them, but before or after, in the correct lane.
- Alleys can cause issues. Use with caution.
- The script spawns 2 entities + 1 emitter for EVERY checkpoint. If you have 100 checkpoints that might just crash peoples games. 

### Track Sharing
You can grab the checkpoints from either My Tracks tab in game, by using the copy button or directly from the database entry and then pasting to something like https://pastebin.com/
There's an import function (if enabled in config) in the Create Track tab to import via paste.

Hop into the [CW Discord](https://discord.gg/FJY4mtjaKr) and share some tracks in the racingapp-tracks channel! 

### User Management
The script offers user management now. We've moved away from the basic/master fob and instead users are saved in the database.
To swap your user, open the racingapp and press the cog-icon to open the settings.
To create users you can either buy a user account from a trader/laptop (if this is enabled in the config) or have someone create one for you.

The tiers are racer < creator < master < god and are defined as follows:
```lua
    racer = { 
        join = true, -- join races
        records = true, -- see records
        setup = true, -- setup races
        create = false, -- create races
        control = false, -- control users
        controlAll = false, -- control all users
    }
    ...
```

*join* means you can join races\
*records* means you can access records\
*setup* means you can set up races\
*create* means you can create tracks\
*control* means you can manage users you create\
*controllAll* allows you to control all users, and also permanently delete users

Basically, any racer name/user created by another player will be tied to them. So if person X buys an account from player Y, player Y can also revoke player Xs account via the in game menus, as long as player Y has a user with the *control* authorization.

## Opening the racing app

# Preview

## Latest video

[![YOUTUBE VIDEO](http://img.youtube.com/vi/nRuM03co7Mk/0.jpg)](https://youtu.be/nRuM03co7Mk)

<details>
  <summary>Older Videos</summary>
  
### Might not represent current looks/design/features
### Note: Before new UI was added

[![YOUTUBE VIDEO](http://img.youtube.com/vi/APtMydz4gF8/0.jpg)](https://youtu.be/APtMydz4gF8)

Update to track editor:
### Note: Before new UI was added

[![YOUTUBE VIDEO](http://img.youtube.com/vi/N_HI0jAsgbg/0.jpg)](https://youtu.be/N_HI0jAsgbg)

### UI Update:

[![YOUTUBE VIDEO](http://img.youtube.com/vi/j0KKvy-2VWc/0.jpg)](https://youtu.be/j0KKvy-2VWc)

### User Management Update:

[![YOUTUBE VIDEO](http://img.youtube.com/vi/YzJjRs2rv2s/0.jpg)](https://youtu.be/YzJjRs2rv2s)

### UI update 2:

[![YOUTUBE VIDEO](http://img.youtube.com/vi/ZAUrmS63ZaM/0.jpg)](https://youtu.be/ZAUrmS63ZaM)

### Ranked, ELO and Crew systems
[![YOUTUBE VIDEO](http://img.youtube.com/vi/gyt_EqFqfds/0.jpg)](https://youtu.be/gyt_EqFqfds)

### Latest UI rework + translations 

[![YOUTUBE VIDEO](http://img.youtube.com/vi/8Vkj0o8VvCY/0.jpg)](https://youtu.be/8Vkj0o8VvCY)

</details>

<details>
<summary>Images</summary>

**Track Setup**

![Track Selection](https://media.discordapp.net/attachments/1202695794537537568/1276957396677431416/image.png?ex=66cb6ac0&is=66ca1940&hm=20eef13f8f901c01833ad31d4f605a0a56b3fb4ec3d6f64bdbe0c76b595f7b2c&=&format=webp&quality=lossless&width=782&height=457)
![Track Setup](https://media.discordapp.net/attachments/1202695794537537568/1276957700118417550/image.png?ex=66cb6b08&is=66ca1988&hm=0eab69671c24ce74ab5c33d6bfc42e2fb5a36ee00c4ccb25079dcd00f914bb4d&=&format=webp&quality=lossless&width=782&height=449)

**Leaderboards**

![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957700449636453/image.png?ex=66cb6b08&is=66ca1988&hm=85f91895299789c78357dba40acf60bb8d0034c03d16c3188a37c1f9acaafb9f&=&format=webp&quality=lossless&width=782&height=455)
![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957700722524223/image.png?ex=66cb6b08&is=66ca1988&hm=7b692b8532a70f503885c4c3c83da96034a6d1d01478b2cdedb4a337348840cd&=&format=webp&quality=lossless&width=782&height=456)
![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957700948889631/image.png?ex=66cb6b08&is=66ca1988&hm=13359ad6b4ddc6aa6addb5e0a06652139b12d7e671f919f5700aca4d362edbc3&=&format=webp&quality=lossless&width=782&height=453)

**Track Creation**

You can create tracks from both using an in-game editor or copy/paste a set of checkpoints.

**Manage Tracks**

![Tracks menu](https://media.discordapp.net/attachments/1202695794537537568/1276957701225844856/image.png?ex=66cb6b08&is=66ca1988&hm=f5f9169f87161c729e7d046bc2e39bde483dba520a83ace50593c4c66471acdb&=&format=webp&quality=lossless&width=782&height=453)

![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957701468979293/image.png?ex=66cb6b08&is=66ca1988&hm=7fe5372955f21e3e5c072a70fc037ddc86573b36bc63f32ee5b4bb33d1765875&=&format=webp&quality=lossless&width=782&height=460)

**Manage Crew**

![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957782611857418/image.png?ex=66cb6b1c&is=66ca199c&hm=ab465e525702acf9499a08d23b56b06abc0b40b2e446d14673d521158b055160&=&format=webp&quality=lossless&width=782&height=473)
![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957782934945812/image.png?ex=66cb6b1c&is=66ca199c&hm=9399c0825a24f0e0e586738976246199a9c4bc5e66e7555eb6ce5463ca8638b1&=&format=webp&quality=lossless&width=782&height=459)
![Interface](https://media.discordapp.net/attachments/1202695794537537568/1276957783224483881/image.png?ex=66cb6b1c&is=66ca199c&hm=a8311e0d10bfde2efef9333e5e761050770d20b8eda10360627070d86c2a6a72&=&format=webp&quality=lossless&width=782&height=470)

**Handle your race users**

![Users](https://media.discordapp.net/attachments/1202695794537537568/1276958004113047573/image.png?ex=66cb6b50&is=66ca19d0&hm=107f3b94d5a0b91741a94186d4744227f34d02884b08f05a44c95fb535ee1595&=&format=webp&quality=lossless&width=782&height=455)
![Users](https://media.discordapp.net/attachments/1202695794537537568/1276958004436140062/image.png?ex=66cb6b50&is=66ca19d0&hm=b0835004148e4c36b89f4fb563d8a337e91c661d735b6158908c122cdbc19631&=&format=webp&quality=lossless&width=782&height=464)

**Settings**

![Settings](https://media.discordapp.net/attachments/1202695794537537568/1276959445729148991/image.png?ex=66cb6ca8&is=66ca1b28&hm=de9240a7be25638c6d302a2a1bddd8d49ebe83590ae0e3b3f6f10dbf563189c3&=&format=webp&quality=lossless&width=782&height=466)


