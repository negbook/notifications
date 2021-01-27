# fxserver-notifications
Notifications utilities for FXServer

![preview](https://github.com/negbook/notifications/blob/main/preview.png?raw=true)

[INSTALLATION]

Set it as a dependency in you fxmanifest.lua

```
client_script '@notifications/notifications.lua'
```

[FUNCTIONS]

```
ShowNotificatioMessagetext(Title, Subitle, CrewString, Content, textureDict, textureName, iconEnum, icon2Enum, textColor,speed)
ShowNotificatioStats(Title, Subitle, oldProgress,newProgress, textureDict, textureName)
ShowNotificationTicker(msg)
ShowNotificationAward((Title,Subitle,xp, txd, txn, colourEnum)
ShowNotificationUnlock(Title,iconIndex,Subitle,colourEnum)
ShowNotificatioCrewRankup(Title, Subitle, textureDict, textureName)
ShowNotificationVersus(textureDict1,textureName1,Scores1,textureDict2,textureName2,Scores2)
ShowNotificatioReplay(subtitle, Icon)
GetHudColor(string)
```

[EXAMPLE]

```
Citizen.CreateThread(function()
    
     ShowNotificatioMessagetext("TITLE","DESCRIPTION","(+#NEGBK","Content",'CHAR_MICHAEL','CHAR_MICHAEL',2,3,GetHudColor('HUD_COLOUR_WHITE'),1.0)
     ShowNotificatioMessagetext("TITLE2","DESCRIPTION2","@*#NEGB","Content2",'CHAR_MICHAEL','CHAR_MICHAEL',2,3,GetHudColor('HUD_COLOUR_WHITE'),1.0)
     ShowNotificatioMessagetext("TITLE3","DESCRIPTION3","#0xNEGB","Content3",'CHAR_MICHAEL','CHAR_MICHAEL',2,3,GetHudColor('HUD_COLOUR_WHITE'),1.0)
     ShowNotificatioStats("Negbook","Scripting Skills",25,70,'CHAR_MICHAEL','CHAR_MICHAEL')
     ShowNotificationTicker("TICKER")
     ShowNotificationAward("GOLD THROPY","YOU GOT AN AWARD!",333, 'CHAR_MICHAEL', 'CHAR_MICHAEL', GetHudColor('HUD_COLOUR_WHITE'))
     ShowNotificationUnlock("UNLOCK",3,"UNLOCKSUB",GetHudColor('HUD_COLOUR_BLUE'))
     ShowNotificatioCrewRankup("Negbook:","YOU DID A GOOD JOB!!!",'CHAR_MICHAEL','CHAR_MICHAEL')
     ShowNotificationVersus('CHAR_FACEBOOK','CHAR_FACEBOOK',66,'CHAR_MICHAEL','CHAR_MICHAEL',33)
     --ShowNotificatioReplay('subtitle',3)
     --ShowNotificatioReplay('subtitle',"~INPUT_TALK~")
end)
```