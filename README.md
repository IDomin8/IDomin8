# IDomin8

### The Ultimate I-Ready Utility

I-Ready Hacks, similar to Nullify and I-Ready Overload, but with many more features, encrypted code that can't be patched, and a cleaner GUI design.

## Instructions

### How to use IDomin8

1. Activate your bookmarks bar if it's not already by pressing `Ctrl + Shift + B`.
2. Create a new bookmark by right-clicking on your bookmarks bar and clicking "Add Site".
3. In the Address or URL section, paste the code below.
4. Name the bookmark "IReady" or something similar.
5. Go into I-Ready and run it.

```javascript
javascript:(function(){var createGui=function(titleText,leftOffset,content){var gui=document.createElement('div');gui.style.cssText='position:fixed;top:0;left:'+(50+leftOffset)+'%;transform:translateX(-50%);width:300px;height:300px;background:linear-gradient(135deg, #8e44ad, #3498db);z-index:9999;box-shadow:0 4px 8px rgba(0,0,0,0.1);padding:20px;font-family:"Segoe UI",sans-serif;border-radius:10px;color:white;overflow:auto';var title=document.createElement('div');title.style.cssText='font-weight:bold;font-size:20px;margin-bottom:20px';title.innerText=titleText;gui.appendChild(title);content.forEach(function(item){var link=document.createElement('a');link.href=item.url;link.innerText=item.name;link.style.cssText='display:block;margin:5px;padding: 10px; border: 2px solid black; border-radius: 5px; color: white; text-decoration:none';link.target='_blank';gui.appendChild(link)});var closeButton=document.createElement('span');closeButton.innerHTML='&#10006;';closeButton.style.cssText='position:absolute;top:10px;right:10px;font-size:20px;color:black;cursor:pointer';closeButton.addEventListener('click',function(){document.querySelectorAll('.custom-gui').forEach(function(g){document.body.removeChild(g);})});gui.appendChild(closeButton);gui.classList.add('custom-gui');var isDragging=false;var offsetX,offsetY;gui.addEventListener('mousedown',function(e){isDragging=true;offsetX=e.clientX-gui.getBoundingClientRect().left;offsetY=e.clientY-gui.getBoundingClientRect().top;});document.addEventListener('mousemove',function(e){if(isDragging){gui.style.left=e.clientX-offsetX+'px';gui.style.top=e.clientY-offsetY+'px';}});document.addEventListener('mouseup',function(){isDragging=false;});document.body.appendChild(gui);return {gui:gui,gamesButton:null}};var mainGui=createGui('Peeify',0,[{name:'Skip Lesson',url:'#'},{name:'Diagnostic Skipper',url:'#'},{name:'Free Iready Games',url:'#'},{name:'Background Changer',url:'#'},{name:'Press "P" to toggle menu',url:'#'},{name:'Farm Minutes',url:'#'}]);var secondaryGui;mainGui.gui.querySelectorAll('a')[0].onclick=function(event){event.preventDefault(); var score = prompt("What score do you want?"); if(score !== null){score = parseInt(score); if(!isNaN(score) && score >= 0 && score <= 100){eval('() => { return ' + score + '}');} else {alert("Please enter a number from the range of 0 - 100.");}}};mainGui.gui.querySelectorAll('a')[1].onclick=function(event){event.preventDefault(); var score = prompt("What score do you want?"); if(score !== null){score = parseInt(score); if(!isNaN(score) && score >= 0 && score >= 0 && score <= 100){eval('() => { return ' + score + '}');} else {alert("Please enter a number from the range of 0 - 100.");}}};mainGui.gui.querySelectorAll('a')[2].onclick=function(event){event.preventDefault(); if(!secondaryGui){secondaryGui=createGui('Free Iready Games',10,[{name:'Galaxy Sprint',url:'https://cdn.i-ready.com/instruction/reward-games/v1.3.x/2/game-lanerunner/'},{name:'Cat Stacker',url:'https://cdn.i-ready.com/instruction/game-catstacker/1.6.x/2/'},{name:'Path Spinners',url:'https://cdn.i-ready.com/instruction/game-hpr/1.4.x/2/'},{name:'Wizard Pinball',url:'https://cdn.i-ready.com/instruction/reward-games/v1.3.x/2/game-bubbles/'},{name:'Dig Site',url:'https://cdn.i-ready.com/instruction/reward-games/v1.3.x/2/game-minedigger/'},{name:'Begooped',url:'https://cdn.i-ready.com/instruction/game-begooped/1.3.x/2/'}]);secondaryGui.gui.style.left='calc(50% + 320px)';var mainShiftX,mainShiftY;function moveAt(pageX,pageY){mainGui.gui.style.left=pageX-mainShiftX+'px';mainGui.gui.style.top=pageY-mainShiftY+'px';secondaryGui.gui.style.left=parseInt(mainGui.gui.style.left)+320+'px';secondaryGui.gui.style.top=mainGui.gui.style.top}mainGui.gui.onmousedown=function(e){mainShiftX=e.clientX-mainGui.gui.getBoundingClientRect().left;mainShiftY=e.clientY-mainGui.gui.getBoundingClientRect().top;function onMouseMove(e){moveAt(e.pageX,e.pageY)};document.addEventListener('mousemove',onMouseMove);document.onmouseup=function(){document.removeEventListener('mousemove',onMouseMove);document.onmouseup=null};};mainGui.gui.ondragstart=function(){return false};}};mainGui.gui.querySelectorAll('a')[3].onclick=function(event){event.preventDefault(); var imageUrl = prompt("Enter the URL of the new background image:"); if(imageUrl !== null){document.getElementById('background-image').src = imageUrl;}};mainGui.gui.querySelectorAll('a')[5].onclick=function(event){event.preventDefault(); farmMinutes(this);};document.body.appendChild(mainGui.gui);document.addEventListener('keydown', function(event) { if (event.key === 'p' || event.key === 'P') { mainGui.gui.style.display = mainGui.gui.style.display === 'none' ? 'block' : 'none'; } });function farmMinutes(button) { if (minuteFarming) { let csid = getCookie("csid"); fetch(`https://login.i-ready.com/student/v1/web/lesson_component/${csid}?action=pause`, { headers: { accept: "application/json, text/plain, */*", "accept-language": "en-US,en;q=0.9", "sec-fetch-dest": "empty", "sec-fetch-mode": "cors", "sec-fetch-site": "same-origin" }, referrer: "https://login.i-ready.com/student/dashboard/home", referrerPolicy: "strict-origin-when-cross-origin", method: "GET", mode: "cors", credentials: "include" }); document.cookie = 'csid=; expires=Thu, 18 Dec 1970 12:00:00 UTC'; button.innerText = "Farm minutes"; minuteFarming = false; alert("The minutes should now be in your account."); } else if (window.html5Iframe) { let csid = html5Iframe.src.split("?csid=")[1].split("&type")[0]; document.cookie = `csid=${csid}; expires=Thu, 18 Dec 2999 12:00:00 UTC`; document.cookie = 'minutes=45; expires=Thu, 18 Dec 2999 12:00:00 UTC'; alert("Necessary data to farm minutes have now been collected. To begin farming minutes, go to the iReady menu by closing this lesson/quiz. Then, press this button again."); } else if (getCookie("csid")) { let csid = getCookie("csid"); fetch(`https://login.i-ready.com/student/v1/web/lesson_component/${csid}?action=resume`, { headers: { accept: "application/json, text/plain, */*", "accept-language": "en-US,en;q=0.9", "sec-fetch-dest": "empty", "sec-fetch-mode": "cors", "sec-fetch-site": "same-origin" }, referrer: "https://login.i-ready.com/student/dashboard/home", referrerPolicy: "strict-origin-when-cross-origin", method: "GET", mode: "cors", credentials: "include" }); minuteFarming = true; button.innerText = "Stop farming minutes"; alert('The minute farming process has now begun. Do not close this page. Do not turn off your computer. After you press "ok," every minute that passes will be added to your account. When you want to stop the timer and add the farmed minutes to your account, press the button labeled "Stop farming minutes". Press "ok" to begin.'); } else { alert("You do not have a lesson currently open. You must open a lesson to begin the process."); }} function getCookie(name) { let value = `; ${document.cookie}`; let parts = value.split(`; ${name}=`); if (parts.length === 2) return parts.pop().split(';').shift(); return ""; } var minuteFarming = false;})();
```

## Features
- Skip lessons and quizzes
- Diagnostic skipper
- Free access to I-Ready games
- Customizable backgrounds
- Minute farming
- Encrypted code to prevent patching
- Clean and intuitive GUI design




## Troubleshooting

### Common Issues

- **Bookmark not working**: Make sure you have copied the entire JavaScript code correctly.
- **Feature not working**: Ensure you are logged into I-Ready and have the necessary permissions.
- **GUI not displaying correctly**: Try refreshing the page or clearing your browser cache.


## Disclaimer
**USE AT YOUR OWN RISK. It's not my fault if you get banned.**
