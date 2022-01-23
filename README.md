# Nice-Blog-Cards

HTML
<div class="card-container">  
  <div class="card card-1">  
   <div class="card-img"></div>  
   <a href="" class="card-link">  
    <div class="card-img-hovered"></div>  
   </a>  
   <div class="card-info">  
    <div class="card-about">  
     <a class="card-tag tag-news">NEWS</a>  
    <div class="card-time">6/1/2022</div>  
    </div>  
    <h1 class="card-title">There have been big Tesla accident at New Jersey</h1>  
    <div class="card-creator">by <a href="">Sardorbek Usmonov</a></div>  
   </div>  
  </div>  
  <div class="card card-2">  
   <div class="card-img"></div>  
   <a href="" class="card-link">  
    <div class="card-img-hovered"></div>  
   </a>  
   <div class="card-info">  
    <div class="card-about">  
     <a class="card-tag">Tech</a>  
    <div class="card-time">6/01/2022</div>  
    </div>  
    <h1 class="card-title">Samsung laptops is exploding again</h1>  
    <div class="card-creator">by <a href="">Tyler Platt</a></div>  
   </div>  
  </div>  
  <div class="card card-3">  
   <div class="card-img"></div>  
   <a href="" class="card-link">  
    <div class="card-img-hovered"></div>  
   </a>  
   <div class="card-info">  
    <div class="card-about">  
     <a class="card-tag tag-deals">Deals</a>  
    <div class="card-time">5/2/2022</div>  
    </div>  
    <h1 class="card-title">Apple is having big Sale for the first time</h1>  
    <div class="card-creator">by <a href="">Timur Mirzoyev</a></div>  
   </div>  
  </div>  
  <div class="card card-4">  
   <div class="card-img"></div>  
   <a href="" class="card-link">  
    <div class="card-img-hovered"></div>  
   </a>  
   <div class="card-info">  
    <div class="card-about">  
     <a class="card-tag tag-politics">Politics</a>  
    <div class="card-time">5/2/2000</div>  
    </div>  
    <h1 class="card-title">Net-Nutrality is coming to its end</h1>  
    <div class="card-creator">by <a href="">Gregoy Trem</a></div>  
   </div>  
  </div>  
 </div>  
 
 CSS
 /* RESET */  
 * {  
  margin: 0;  
  padding: 0;  
  box-sizing: border-box;  
 }  
 body {  
  background: #ebecf0;  
  font-family: "Open Sans", sans-serif;  
  min-height: 100vh;  
 }  
 body a {  
  text-decoration: none;  
  color: #172b4d;  
 }  
 body h1 {  
  font-family: "Song Myung", serif;  
 }  
 /* DEFAULT STYLE */  
 :root {  
  font-size: 16px;  
  --card-img-height: 200px;  
 }  
 .card-container {  
  width: 100%;  
  height: 100vh;  
  display: flex;  
  flex-flow: row wrap;  
  justify-content: center;  
  align-items: center;  
  transition: all 200ms ease-in-out;  
 }  
 .card {  
  align-self: flex-start;  
  position: relative;  
  width: 325px;  
  min-width: 275px;  
  margin: 1.25rem 0.75rem;  
  background: white;  
  transition: all 300ms ease-in-out;  
 }  
 .card .card-img {  
  visibility: hidden;  
  width: 100%;  
  height: var(--card-img-height);  
  background-repeat: no-repeat;  
  background-position: center center;  
  background-size: cover;  
 }  
 .card .card-img-hovered {  
  --card-img-hovered-overlay: linear-gradient(  
   to bottom,  
   rgba(0, 0, 0, 0),  
   rgba(0, 0, 0, 0)  
  );  
  transition: all 350ms ease-in-out;  
  background-repeat: no-repeat;  
  background-position: center center;  
  background-size: cover;  
  width: 100%;  
  position: absolute;  
  height: var(--card-img-height);  
  top: 0;  
 }  
 .card .card-info {  
  position: relative;  
  padding: 0.75rem 1.25rem;  
  transition: all 200ms ease-in-out;  
 }  
 .card .card-info .card-about {  
  display: flex;  
  justify-content: space-between;  
  align-items: center;  
  padding: 0.75rem 0;  
  transition: all 200ms ease-in-out;  
 }  
 .card .card-info .card-about .card-tag {  
  width: 60px;  
  max-width: 100px;  
  padding: 0.2rem 0.5rem;  
  font-size: 12px;  
  text-align: center;  
  text-transform: uppercase;  
  letter-spacing: 1px;  
  background: #505f79;  
  color: #fff;  
 }  
 .card .card-info .card-about .card-tag.tag-news {  
  background: #36b37e;  
 }  
 .card .card-info .card-about .card-tag.tag-deals {  
  background: #ffab00;  
 }  
 .card .card-info .card-about .card-tag.tag-politics {  
  width: 71px;  
  background: #ff5630;  
 }  
 .card .card-info .card-title {  
  z-index: 10;  
  font-size: 1.5rem;  
  padding-bottom: 0.75rem;  
  transition: all 350ms ease-in-out;  
 }  
 .card .card-info .card-creator {  
  padding-bottom: 0.75rem;  
  transition: all 250ms ease-in-out;  
 }  
 .card:hover {  
  cursor: pointer;  
  box-shadow: 0px 15px 35px rgba(227, 252, 239, 0.1), 0px 5px 15px rgba(0, 0, 0, 0.07);  
  transform: scale(1.025);  
 }  
 .card:hover .card-img-hovered {  
  --card-img-hovered-overlay: linear-gradient(  
   to bottom,  
   rgba(0, 0, 0, 0),  
   rgba(0, 0, 0, 0.65)  
  );  
  height: 100%;  
 }  
 .card:hover .card-about,  
 .card:hover .card-creator {  
  opacity: 0;  
 }  
 .card:hover .card-info {  
  background-color: transparent;  
 }  
 .card:hover .card-title {  
  color: #ebecf0;  
  transform: translate(0, 40px);  
 }  
 .card-1 .card-img,  
 .card-1 .card-img-hovered {  
  background-image: var(--card-img-hovered-overlay), url(https://source.unsplash.com/Qm_n6aoYzDs);  
 }  
 .card-2 .card-img,  
 .card-2 .card-img-hovered {  
  background-image: var(--card-img-hovered-overlay), url(https://source.unsplash.com/C-v1p2DTakA);  
 }  
 .card-3 .card-img,  
 .card-3 .card-img-hovered {  
  background-image: var(--card-img-hovered-overlay), url(https://source.unsplash.com/V0L1LH7qWOQ);  
 }  
 .card-4 .card-img,  
 .card-4 .card-img-hovered {  
  background-image: var(--card-img-hovered-overlay), url(https://source.unsplash.com/zAi2Is48-MA);  
 }  
