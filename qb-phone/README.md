# qb-phone
Разширен телефон за QB-Core Framework :iphone:

# Лиценз

    QBCore Framework
    Авторско право (C) 2023ufi

    Тази програма е свободен софтуер: можете да я разпространявате и/или модифицирате
    съгласно условията на Общия публичен лиценз на GNU, публикуван от
    Фондацията за свободен софтуер, или версия 3 на Лиценза, или
    (по ваш избор) всяка по-късна версия.

    Тази програма се разпространява с надеждата, че ще бъде полезна,
    но БЕЗ КАКВАТО И ДА Е ГАРАНЦИЯ; дори без подразбиращата се гаранция за
    ТЪРГОВСКА ДОСТОЙНОСТ или ПРИГОДНОСТ ЗА КОНКРЕТНА ЦЕЛ.  Вижте
    GNU General Public License за повече подробности.

    Трябва да сте получили копие от Общия публичен лиценз на ГНУ
    заедно с тази програма.  Ако не, вижте <https://www.gnu.org/licenses/>

## Зависимости
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-policejob](https://github.com/qbcore-framework/qb-policejob) - MEOS, проверка на белезници и др. 
- [qb-crypto](https://github.com/qbcore-framework/qb-crypto) - Търговия с криптовалути 
- [qb-lapraces](https://github.com/qbcore-framework/qb-lapraces) - Създаване на маршрути и състезания 
- [qb-houses](https://github.com/qbcore-framework/qb-houses) - Приложение за управление на къщи и ключове
- [qb-garages](https://github.com/qbcore-framework/qb-garages) - Приложение за гаражи
- [qb-banking](https://github.com/qbcore-framework/qb-banking) - За приложение за банкиране
- [screenshot-basic](https://github.com/citizenfx/screenshot-basic) - За правене на снимки
- Webhook за хостване на снимки (Discord или Imgur могат да осигурят това)


## Снимки на екрана
![Home](https://cdn.discordapp.com/attachments/921675245360922625/921675439783673897/home.jpg)
![Bank](https://cdn.discordapp.com/attachments/921675245360922625/921675441142644756/bank.jpg)
![Advert](https://cdn.discordapp.com/attachments/921675245360922625/921675440878415872/advert.jpg)
![Mail](https://cdn.discordapp.com/attachments/921675245360922625/921675440278614068/mail.jpg)
![Garage](https://cdn.discordapp.com/attachments/921675245360922625/921675439590760528/garage.jpg)
![Garage Detail](https://cdn.discordapp.com/attachments/921675245360922625/921675441591422986/garage_in.jpg)
![services](https://cdn.discordapp.com/attachments/921675245360922625/921675458670641152/services.jpg)
![Houses](https://cdn.discordapp.com/attachments/921675245360922625/921675440005988362/house.jpg)
![Racing](https://cdn.discordapp.com/attachments/921675245360922625/921675458423173140/race.jpg)
![Crypto](https://cdn.discordapp.com/attachments/921675245360922625/921675457718517820/qbit.jpg)
![Gallery](https://cdn.discordapp.com/attachments/921675245360922625/921675441381736448/gallery.jpg)
![MEOS](https://cdn.discordapp.com/attachments/921675245360922625/921675440488341534/meos.jpg)
![Twitter](https://cdn.discordapp.com/attachments/921675245360922625/921675459270438922/twitter.jpg)
![Settings]

Translated with www.DeepL.com/Translator (free version)
```
ensure qb-core
ensure screenshot-basic
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
## Setup Webhook in `server/main.lua` for photos
Set the following variable to your webhook (For example, a Discord channel or Imgur webhook)
### To use Discord:
- Right click on a channel dedicated for photos
- Click Edit Channel
- Click Integrations
- Click View Webhooks
- Click New Webhook
- Confirm channel
- Click Copy Webhook URL
- Paste into `WebHook` in `server/main.lua`
```
local WebHook = ""
```
