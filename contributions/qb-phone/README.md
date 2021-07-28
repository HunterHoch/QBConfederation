# qb-phone
Advanced Phone for QB-Core Framework :iphone:

## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-policejob](https://github.com/qbcore-framework/qb-policejob) - MEOS, handcuff check etc. 
- [qb-crypto](https://github.com/qbcore-framework/qb-crypto) - Crypto currency trading 
- [qb-lapraces](https://github.com/qbcore-framework/qb-lapraces) - Creating routes and racing 
- [qb-houses](https://github.com/qbcore-framework/qb-houses) - House and key management 
- [qb-garages](https://github.com/qbcore-framework/qb-garages) - 
- [qb-banking](https://github.com/qbcore-framework/qb-banking) - For banking


## Screenshots
![Home](https://i.imgur.com/glglNdH.png)
![Bank](https://i.imgur.com/5m1STgM.png)
![Messages](https://i.imgur.com/oYHfjKd.png)
![Phone](https://i.imgur.com/qnpRzRj.png)
![Settings](https://i.imgur.com/Z9cOcWp.png)
![MEOS](https://i.imgur.com/BfES1CS.png)
![Vehicles](https://i.imgur.com/HpSM1qt.png)
![Email](https://i.imgur.com/Ai2ixMz.png)
![Advertisements](https://i.imgur.com/KOlvicw.png)
![Houses](https://i.imgur.com/B4aTGo0.png)
![App Store](https://imgur.com/mpBOgfN.png)
![Lawyers](https://i.imgur.com/nWZKCQh.png)
![Racing](https://i.imgur.com/Yif8SYn.png)
![Crypto](https://i.imgur.com/9irWkTD.png)

## Features
- Garages app to see your vehicle details
- Mails to inform the player
- Banking app to see balance and transfer money
- Racing app to create races
- App Store to download apps
- MEOS app for polices to search
- Houses app for house details and management

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-phone.sql` in your database
- Add the following code to your server.cfg/resouces.cfg
```
ensure qb-core
ensure qb-phone
ensure qb-policejob
ensure qb-crypto
ensure qb-lapraces
ensure qb-houses
ensure qb-garages
ensure qb-banking
```

## Configuration
```

Config = Config or {}

Config.RepeatTimeout = 2000 -- Timeout for unanswered call notification
Config.CallRepeats = 10 -- Repeats for unanswered call notification
Config.OpenPhone = 244 -- Key to open phone display
Config.PhoneApplications = {
    ["phone"] = { -- Needs to be unique
        app = "phone", -- App route
        color = "#04b543", -- App icon color
        icon = "fa fa-phone-alt", -- App icon
        tooltipText = "Phone", -- App name
        tooltipPos = "top",
        job = false, -- Job requirement
        blockedjobs = {}, -- Jobs cannot use this app
        slot = 1, -- App position
        Alerts = 0, -- Alert count
    },
}
```
