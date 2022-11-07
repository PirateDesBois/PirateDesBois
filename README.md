![](https://github.com/PirateDesBois/PirateDesBois/blob/main/mygif.gif?raw=true)
<h1 align="center">Hi 👋, I'm Nicola</h1>
<h3 align="center">Design and development Creator</h3>

<p align="center">I am a young full stack developer fresh out of training. I code in react, laravel, and what I enjoy above all is working on the appearance of websites.</p>

<h4 align="center">Skills: LARAVEL / REACT / JS / HTML / CSS / SASS</h4>

<div align="center">
  - 🔭 I’m currently working on My skills <br>
- 🌱 I’m currently learning Deployment of my sites 
</div>
</br>
<p align="center">
<a href="https://linkedin.com/in/https://www.linkedin.com/in/nicola-sieben" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/nicola-sieben" height="30" width="40" /></a>
<a href="https://fb.com/https://www.facebook.com/nicola.sieben/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="https://www.facebook.com/nicola.sieben/" height="30" width="40" /></a>
<a href="https://instagram.com/https://www.instagram.com/diaphragmcreationphotography/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="https://www.instagram.com/diaphragmcreationphotography/" height="30" width="40" /></a>
</p>

<h3 align="center">Languages and Tools:</h3>
<p align="center"> <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://heroku.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/heroku/heroku-icon.svg" alt="heroku" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://www.adobe.com/in/products/illustrator.html" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" alt="illustrator" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> </p>

<div align="center">
  <p><img align="center" src="https://github-readme-stats.vercel.app/api/top-langs?username=piratedesbois&show_icons=true&locale=en&layout=compact" alt="piratedesbois" /></p></br>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=piratedesbois&show_icons=true&locale=en" alt="piratedesbois" /></p></br>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=piratedesbois&" alt="piratedesbois" /></p></br>
</div>






![Profile views](https://gpvc.arturio.dev/PirateDesBois)  


let [chart, widgetSize, theme, weeks] = (args.widgetParameter || "")
  .split(",")
  .map((v) => v.trim());
chart = chart || "calendar";
widgetSize = widgetSize || "medium";
theme = theme || "green";
const darkMode = Device.isUsingDarkAppearance();
let url = `https://ssr-contributions-svg.vercel.app/_/CatsJuice?format=jpeg&quality=2&theme=${theme}&widget_size=${widgetSize}&chart=${chart}&dark=${darkMode}`;

if (weeks) url += `&weeks=${weeks}`;

let w = await createWidget();
Script.setWidget(w);

async function createWidget() {
  let w = new ListWidget();
  let random = (Math.random() * 100000000).toFixed(0);
  let data = await new Request(url + "&random=" + random).load();
  let image = Image.fromData(data);
  w.backgroundImage = image;
  return w;
}
