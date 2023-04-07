<template>
 <div class="container-fluid">
<div class="row">
    <div class="col-lg-8 home-page">
        <div class="shadow p-1 mb-3 bg-white home-shadow">
            <div class="row d-flex">
                <div class="col-lg-8 text-left home-firstOne">
                    <h5>Home</h5>
                </div>
                <div class="col-lg-4 text-right">
                    <div class="home-firsttwo">
                        <i class="fa fa-star-o"></i>
                    </div>
                </div>
                
            </div>
        </div>
        <div class="row tweet">
        <div class="col-lg-1">
            <div class="tweet-image">
                <img src="https://e7.pngegg.com/pngimages/799/987/png-clipart-computer-icons-avatar-icon-design-avatar-heroes-computer-wallpaper-thumbnail.png" alt="">
            </div>
        </div>
        <div class="col-lg-11">
           <div class="tweet-post">
            <div class="form-group">
                <select class="form-control" id="exampleFormControlSelect1">
                <option>Everyone</option>
                <option>Friends</option>
                <option>Private</option>
                <option>demo</option>
                <option>test</option>
                </select>
            </div>
            <textarea
        maxlength="280"
        name=""
        id=""
        cols="28"
        rows="100"
        placeholder="what happening?"
      ></textarea>
           </div>
        </div>
        </div>
        <div class="social-menu p-3">
        <ul>
            <li><a ><i class="fa fa-picture-o"></i></a></li>
            <li><a ><i class="fa fa-video-camera"></i></a></li>
            <li><a ><i class="fa fa-file-text"></i></a></li>
            <li><a ><i class="fa fa-calendar"></i></a></li>
            <li><a ><i class="fa fa-map-marker"></i></a></li>
            <li><a ><i class="fa fa-tag"></i></a></li>
        </ul>
        <div class="tweet-button">
            <button>Tweet</button>
        </div>
    </div>
    <hr class="hr1">
    <div class="text-center">
        <h6 class="text-info font-weight-bold">Show 1234 Post</h6>
    </div>
    <hr>
    <div id="post">
  <div class="header">
    <div class="left-info">
      <div class="thumbnail">
        <img src="https://avatarfiles.alphacoders.com/131/131892.jpg" alt>
      </div>
      <div class="name-info">
        <div class="name">
          <a href="">Nikesh Sharma</a><i class="fa fa-check-circle ml-1" style="font-size:12px;color:#1d9bf0"></i>
        </div>
        <div class="time">
          Noida 12:45 am
          <i class="global-icon ml-1"></i>
        </div>
      </div>
    </div>
    <div class="right-info"></div>
  </div>

  <div class="content">WHY SO SERIOUS?</div>
  <a class="video-link" href="https://youtu.be/UnjzmmK7TaY" target="_blank">
    <div class="video-wrposter">
      <div class="video-thumbnail">
        <img src="https://img.shop.com/Image/250000/257700/257781/products/1545411058__400x400__.jpg" alt="">
      </div>
      <div class="video-info">
        <div class="youtube-title">YOUTUBE.COM</div>
        <div class="video-title">Joker【Let's Play a Game】- Official Video</div>
        <div class="video-desc">"Do I really look like a guy with a plan? You know what I am? I'm a dog chasing cars. I wouldn't know what to do with one if I caught it! You know, I just...DO things."</div>
      </div>
    </div>
  </a>

  <div class="feedback-info">
    <div class="feedback-emojis">
      <i class="icons laugh-icon"></i>
      <i class="icons angry-icon"></i>
      <i class="icons wow-icon"></i>
      Tony Stark, Logan and 9487 others
    </div>
    <div class="threads-and-share">
      <div class="threads"> 15 comments</div>
    </div>
  </div>

  <div class="feedback-action">
    <div class="option">
      <i class="fb-icon thumb-up fa fa-thumbs-up" @click="onLike"></i> {{ counter }}
    </div>
    <div class="option">
      <i class="fb-icon fa fa-retweet" @click="onRetweet"></i> {{ retweet }}
    </div>
    <div class="option">
      <i class="fb-icon response fa fa-comments-o" @click="onComments"></i> 122
    </div>
    <div class="option">
      <i class="fb-icon fa fa-share"></i>
    </div>
  </div>

  <div class="comments" v-if="comments">
    <div class="my-comment-wrposter">
      <div class="my-avatar">
        <img src="https://avatarfiles.alphacoders.com/813/81320.jpg" alt>
      </div>
      <div class="my-comment">
        <div class="my-comment-placeholder">
          <input type="text" placeholder="Write a comment...">
        </div>
      </div>
    </div>
    <div class="wrposter">
      <div class="people-comment-wrposter">
        <div class="people-avatar">
          <img src="https://i1.sndcdn.com/avatars-000472635192-bk5zvc-t500x500.jpg" alt>
        </div>
        <div class="people-comment">
          <div class="people-comment-container">
            <div class="people-name">
              <a href="https://www.facebook.com/Thanos-66479565036/">Aman</a>
              <i class="blue-check"></i>
            </div>
            <div class="people-saying">You're not the only one cursed with knowledge.</div>
          </div>
          <div class="comment-reactions">
            <i class="icons like-icon"></i>
            <span class="number">87</span>
          </div>
        </div>
      </div>
      <div class="like-and-response-wrposter">
        <div class="like-comment">
          <a>Like</a>
          <span class="tiny-dot">・</span>
        </div>
        <div class="day-comment">4 Days</div>
      </div>
    </div>
    <div class="wrposter">
      <div class="people-comment-wrposter">
        <div class="people-avatar">
          <img src="https://avatarfiles.alphacoders.com/123/thumb-123732.jpg" alt>
        </div>
        <div class="people-comment">
          <div class="people-comment-container">
            <div class="people-name">
              <a href="https://www.facebook.com/Thanos-66479565036/">Vipin</a>
              <i class="blue-check"></i>
            </div>
            <div class="people-saying">Bad shit hpostens to people I care about and I don't care about.</div>
            <div class="people-sharing">
              <img src="https://i.ytimg.com/vi/X2Z3aBA9AZE/maxresdefault.jpg" alt="">
            </div>
          </div>
          <div class="comment-reactions">
            <i class="icons like-icon"></i>
            <span class="number">948</span>
          </div>
        </div>
      </div>
      <div class="like-and-response-wrposter">
        <div class="like-comment">
          <a>Like</a>
          <span class="tiny-dot">・</span>
        </div>
        <div class="day-comment">5 Days</div>
      </div>
    </div>
  </div>
</div>
    </div>
    <div class="col-lg-4">
     <div  class="shadow-none p-2 mb-3 bg-white home-shadow">
      <div class="wrapper">

<div class="searchBar">
  <input id="searchQueryInput" type="text" name="searchQueryInput" placeholder="Search" value="" />
  <button id="searchQuerySubmit" type="submit" name="searchQuerySubmit">
    <svg style="width:24px;height:24px" viewBox="0 0 24 24"><path fill="#666666" d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z" />
    </svg>
  </button>
</div>
</div> 
     </div>
     <div class="right-feed mt-5">
     <div class="p-2 text-left">
      <h5 class="font-weight-bold text-dark">What's happening?</h5>
     </div>
     </div>
     <RightSide/>
    </div>
</div>
 </div>
</template>
<script>
import RightSide from '../views/RightSide.vue';
export default {
  components:{
    RightSide
  },
    data(){
      return{
        counter: 20,
        retweet:12,
        comments:false,
      }
    },
    methods:{
      onComments(){
        this.comments = true;
      },
      onLike() { 
        this.counter++;
      },
      onRetweet(){
        this.retweet++;
      },
    }
}
</script>
<style>
.home-page{
   border-left: 1px solid #cecece;
   border-right: 1px solid #cecece;
   border-bottom: 1px solid #cecece;
}
.home-shadow{
    margin-left: -15px;
    margin-right: -15px;
    position: fixed; 
    top: 0px;
    width: 665px;
    z-index: 2;
}
.home-firstOne h5{
    font-weight: 600;
    font-size: 18px;
    font-family: Roboto;
    line-height: 24px;
    margin-left: 8px;
}
.home-firsttwo i{
    font-size: 16px;
    line-height: 26px;
    margin-top: 8px;
    margin-right: 8px;
}

.tweet-image img{
    height: 60px;
    width: 60px;
    border-radius: 50%;
    position: relative;
    top: 14px;
    float: left;
    border: 1px solid #cecece;
    margin-left: -10px;
}
.tweet-post select{
    width:170px;
    position: relative;
    top: 20px;
    margin-left: 10px;
    border-radius:36px;
  overflow:hidden;
  border:1px solid #1d9bf0;
  height: 26px;
  font-size: 12px;

}

textarea {
  padding: 15px;
  font-size: 20px;
  width: 540px;
  height: 60px;
  border: none;
  color: #444;
  resize: none;
  z-index: 1;
  border-radius: 1px;
  margin-top: 10px;
  margin-left: -18px;
}
textarea:focus{
    border: none;
    outline: none;
  }

.tweet {
  position: relative;
  display: flex;
  margin-top: 9%;
  margin-left: -15px;
  margin-right: -15px;
  width: 650px;
}
.social-menu ul{

    display: flex;
}

.social-menu ul li{
    list-style: none;
    margin: 0 15px;
}

.social-menu ul li .fa{
    font-size: 18px;
    line-height: 60px;
    transition: .3s;
    color: #75bbea;
}

.social-menu ul li .fa:hover{
    color: #1d9bf0;
}

.social-menu ul li a{
    position: relative;
    display: block;

}
.tweet-button button{
    background-color: #75bbea;
  border: none;
  color: white;
  padding: 6px 21px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  font-weight: bold;
  margin: 4px 2px;
  cursor: pointer;
  float: right;
  margin-top: -65px;
  border-radius:25px;
}
.tweet-button button:hover{
    background-color: #1d9bf0; 
}
.hr1{
    margin-top:-28px;
}

#post {
  width: 641px;
  background: white;
  padding-bottom: 12px;
  border: 1px solid #dddfe2;
  border-radius: 4px;
}

/* Header */

#post .header {
  display: flex;
  justify-content: space-between;
  padding: 12px 12px 0;
}

#post .header .left-info {
  display: flex;
  justify-content: center;
  align-items: center;
}

#post .header .left-info .thumbnail img {
  display: block; /* img 預設為 inline */
  width: 40px;
  height: 40px;
  margin-right: 8px;
  border-radius: 50%;
}

#post .header .left-info .name-info .name a {
  font-weight: bolder;
  text-decoration: none;
  color: #1d9bf0;
}

#post .header .left-info .name-info .name a:hover {
  text-decoration: underline;
}

#post .header .left-info .name-info .time {
  color: #616770;
  font-size: 13px;
  display: flex;
  justify-content: center;
  align-items: center;
}

#post .header .left-info .name-info .time .global-icon {
  width: 12px;
  height: 12px;
  background-position: -28px -499px;
  background-image: url("https://weichiachang.github.io/easter-eggs-mobile/images/3o8Zo7X.png");
  background-size: 73px 540px;
  background-repeat: no-repeat;
  display: inline-block;
}

#post .header .right-info {
  background-image: url("https://weichiachang.github.io/easter-eggs-mobile/images/dNpCLDT.png");
  background-repeat: no-repeat;
  background-size: 500px 287px;
  background-position: -242px -245px;
  width: 20px;
  height: 20px;
  cursor: pointer;
}

/* Content */

#post .content {
  font-size: 14px;
  font-weight: 300;
  line-height: 20px;
  margin: 12px 12px 7px;
  float: left;
}

#post .video-link {
  text-decoration: none;
}

#post .video-link .video-wrposter {
  display: flex;
  background: #f2f3f5;
  width: 641px;
  height: 139px;
}

#post .video-link .video-wrposter .video-thumbnail img {
  width: 139px;
  height: 139px;
}

#post .video-link .video-wrposter .video-info {
  padding: 10px 12px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-top: 1px solid #dddfe2;
  border-bottom: 1px solid #dddfe2;
}

#post .video-link .video-wrposter .video-info .youtube-title {
  color: #606770;
  font-size: 13px;
  line-height: 16px;
}

#post .video-link .video-wrposter .video-info .video-title {
  color: #1d2129;
  font-weight: bolder;
  font-size: 17px;
  line-height: 20px;
  margin-top: 2px;
}

#post .video-link .video-wrposter .video-info .video-desc {
  color: #606770;
  font-size: 15px;
  line-height: 20px;
  margin-top: 3px;
  min-height: 40px;
  width: 330px;
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}

/* Feedback */

#post .feedback-info {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #dadde1;
  margin: 10px 12px 0 12px;
  padding: 0 0 10px 0;
  color: #938FA4;
}

#post .feedback-info .feedback-emojis {
  min-width: 100px;
  font-size: 14px;
  display: flex;
  align-items: center;
}

#post .feedback-info .feedback-emojis .icons.laugh-icon {
  background-image: url("https://i.imgur.com/KNd9mL2.png");
  background-repeat: no-repeat;
  background-size: 49px 660px;
  height: 16px;
  width: 16px;
  line-height: 16px;
  margin-left: -2px;
  margin-right: 2px;
  background-position: -17px -475px;
}

#post .feedback-info .feedback-emojis .icons.angry-icon {
  background-image: url("https://i.imgur.com/KNd9mL2.png");
  background-repeat: no-repeat;
  background-size: 49px 660px;
  height: 16px;
  width: 16px;
  line-height: 16px;
  margin-left: -4px;
  margin-right: 2px;
  background-position: -17px -441px;
}

#post .feedback-info .feedback-emojis .icons.wow-icon {
  background-image: url("https://i.imgur.com/KNd9mL2.png");
  background-repeat: no-repeat;
  background-size: 49px 660px;
  height: 16px;
  width: 16px;
  line-height: 16px;
  margin-left: -4px;
  margin-right: 4px;
  background-position: 0 -543px;
}


#post .feedback-info .threads-and-share {
  font-size: 14px;
}

#post .feedback-action {
  display: flex;
  justify-content: space-around;
  align-items: center;
  color: #606770;
  font-weight: 600;
  font-size: 14px;
  height: 32px;
  padding: 4px 12px;
}

#post .feedback-action div {
  cursor: pointer;
}

#post .feedback-action .fb-wrposter {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  min-height: 32px;
}

#post .feedback-action .fb-wrposter:hover {
  background-color: rgba(29, 33, 41, 0.04);
  border-radius: 2px;
  text-decoration: none;
}
#post .feedback-action .option{
  font-size: 14px;
}
#post .feedback-action .option:hover{
  color: #1d9bf0;
}

#post .feedback-action .fb-wrposter .fb-icon {
  width: 18px;
  height: 18px;
  display: inline-block;
  background-repeat: no-repeat;
  margin-right: 6px;
  font-size: 18px;
}

#post .feedback-action .fb-wrposter .fb-icon.share {
  background-image: url("https://i.imgur.com/1V94KpF.png");
  background-size: 161px 376px;
  background-position: -61px -249px;
}

#post .comments {
  margin: 0 12px;
  border-top: 1px solid #dadde1;
}

#post .comments .my-comment-wrposter {
  display: flex;
  align-items: center;
  margin-top: 12px;
}

#post .comments .my-comment-wrposter .my-avatar img {
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: block;
  margin-right: 6px;
}

#post .comments .my-comment-wrposter .my-comment {
  background-color: #f2f3f5;
  border: 1px solid #ccd0d5;
  border-radius: 17px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: text;
  flex: auto;
  line-height: 16px;
  padding: 7px 12px;
}

#post .my-comment-wrposter .my-comment .my-comment-placeholder input[type=text] {
  width: 410px;
  outline: none;
  border: 0 solid transparent;
  background: transparent;
}

#post .comments .people-comment-wrposter {
  display: flex;
  align-items: flex-start;
  margin-top: 10px;
}

#post .comments .people-comment-wrposter .people-avatar img {
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: block;
  margin-right: 6px;
}

#post .comments .people-comment-wrposter .people-comment {
  background: #f2f3f5;
  border-radius: 18px;
  color: #1c1e21;
  line-height: 16px;
  padding: 8px 12px;
  position: relative;
}

#post .people-comment-wrposter .people-comment .people-comment-container {
  color: #1c1e21;
  font-size: 12px;
  display: flex;
  flex-direction: column;
  float: left;
}

#post .people-comment-wrposter .people-comment .people-comment-container .people-name {
  font-weight: 600;
  margin-right: 4px;
}

#post .people-comment-wrposter .people-comment .people-comment-container .people-name a {
  text-decoration: none;
  color: #1d9bf0;
  float: left;
}

#post .people-comment-wrposter .people-comment .people-comment-container .people-name:hover {
  text-decoration: underline;
}

#post .people-comment-wrposter .people-comment .people-comment-container .people-name .blue-check {
  margin-left: 4px; 
  background-image: url("https://i.imgur.com/xgnUC5P.png");
  background-repeat: no-repeat;
  background-size: 28px 195px;
  background-position: 0 -165px;
  height: 15px;
  vertical-align: -2px;
  width: 15px;
  display: inline-block;
  float: left;
}

#post .people-comment-wrposter .people-comment .people-comment-container .people-sharing img {
  width: 350px;
}

#post .people-comment-wrposter .people-comment .comment-reactions {
  position: absolute;
  bottom: 4px;
  right: -25px;
  z-index: 9999;
  display: flex;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.2);
  color: #8d949e;
  font-size: 12px;
  padding: 2px 1px 2px 4px;
}

#post .people-comment-wrposter .people-comment .comment-reactions .icons.like-icon {
  background: #fff;
  border-radius: 12px;
  box-shadow: 2px 0 white;
  overflow: hidden;
  background-image: url("https://i.imgur.com/KNd9mL2.png");
  background-repeat: no-repeat;
  background-size: 49px 660px;
  background-position: 0 -526px;
  cursor: pointer;
  height: 16px;
  width: 16px;
  line-height: 16px;
  display: inline-block;
  margin-left: -2px;
  margin-right: 2px;
}

#post .people-comment-wrposter .people-comment .comment-reactions .number {
  padding: 0 3px 0 2px;
}

#post .like-and-response-wrposter {
  display: flex;
  color: #90949c;
  font-size: 13px;
  line-height: 13px;
  margin: 5px 0 0 50px;
}

#post .like-and-response-wrposter .tiny-dot {
  margin-left: -2px;
  margin-right: 2px;
  color: #8d949e;
}
 
#post .like-and-response-wrposter .like-comment {
  color: #1d9bf0;
  cursor: pointer;
}
/* ---------right section---------- */    
.wrapper {
  width: 50%;
    max-width: 21.25rem;
    position: fixed;
    top: 5px;
    z-index: 2; 
 
}

.label {
  font-size: .625rem;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: +1.3px;
  margin-bottom: 1rem;
}

.searchBar {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
}

#searchQueryInput {
  width: 100%;
  height: 2.8rem;
  background: #f5f5f5;
  outline: none;
  border: none;
  border-radius: 1.625rem;
  padding: 0 3.5rem 0 1.5rem;
  font-size: 1rem;
}

#searchQuerySubmit {
  width: 3.5rem;
  height: 2.8rem;
  margin-left: -3.5rem;
  background: none;
  border: none;
  outline: none;
}

#searchQuerySubmit:hover {
  cursor: pointer;
}



 
</style>