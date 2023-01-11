<template>
<div class="container">
  <div class="menu">
    <div class="page-title">
      <img src="./assets/layout.svg"  alt="dashboard icon" />
      <h1>Dashboard</h1>
    </div>
    <div class="user-menu">
      <div v-for="item in userMenu" :key="item" class="item">
        <img :src='require(`./assets/` + item.icon)' alt="" />
        <div class="title">{{ item.title }}</div>
      </div>
    </div>
    <div class="app-menu">
      <div v-for="item in appMenu" :key="item" class="item">
        <img :src='require(`./assets/` + item.icon)' alt="" />
        <div class="title">{{ item.title }}</div>
      </div>
    </div>
  </div>
  <div class="dash-container">
    <div class="up-menu">
      <div class="search">
        <div class="icon">
          <img src="./assets/search.svg" />
        </div>
        <div class="bar">
          <input type="text" name="search-input" id="search">
        </div>
      </div>
      <div class="user-menu">
        <div class="notification">
          <img src="./assets/bell.svg" alt="" />
        </div>
        <div class="user-profile">
          <div class="user-icon">
            <img src="./assets/icon.jpg" />
          </div>
          <div class="user-full-name">Ipsum Loremipsum</div>
        </div>
      </div>
    </div>
    <div class="lower-menu">
      <div class="user">
        <div class="user-icon">
          <img src="./assets/icon.jpg" alt="">
        </div>
        <div class="welcome-message">
          Hi there,
        </div>
        <div class="name">Ipsum Loremipsum (@loremipsum)</div>
      </div>
      <div class="post-buttons">
        <button class="btn-up">New</button>
        <button class="btn-up">Upload</button>
        <button class="btn-up">Share</button>
      </div>
    </div>
    <div class="dashboard">
    <div class="projects">
      <h2 class="label">Your Projects</h2>
    <div class="container">
      <div v-for="i in 5" :key="i" class="item">
        <div class="project-info">
          <h3>Super Cool Project</h3>
          <div class="summary">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Saepe libero recusandae in nesciunt officia deserunt nulla, et animi aliquid deleniti.
          </div>
        </div>
        <div class="project-menu">
          <div class="star">
            <img src="./assets/star.svg" alt="" />
          </div>
          <div class="watch">
            <img src="./assets/eye.svg" alt="" />
          </div>
          <div class="share">
            <img src="./assets/share-2.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
    </div>
    <div class="announce">
      <h2>Announcements</h2>
      <div class="ann-container">
        <div v-for="i in 3" :key="i" class="item">
          <h4>Site Maintence</h4>
          <div class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur corrupti aperiam, facere temporibus rerum quae?</div>
        </div>
      </div>

    </div>
    <div class="trend">
      <h2>Trending</h2>
      <div class="trend-container">
        <div v-for="i in 5" :key="i" class="item">
          <div class="icon">
            <img src="./assets/user-icon.png" />
          </div>
          <div class="name">
            <h4>@ipsumlorem</h4>
            <p>Albert Bookshetd</p></div>
        </div>
      </div>
    </div>
    </div>
  </div>
</div>
</template>

<script setup>
const userMenu = [
  { icon: 'house.svg', title: 'Home'},
  { icon: 'user.svg', title: 'Profile' },
  { icon: 'message.svg', title: 'Messages' },
  { icon: 'watch.svg', title: 'History' },
  { icon: 'paper-note.svg', title: 'Tasks' },
  { icon: 'people.svg', title: 'Communities' }
];
const appMenu = [
  { icon: 'settings.svg', title: 'Setting' },
  { icon: 'question.svg', title: 'Support' },
  { icon: 'shield.svg', title: 'Privacy' },

]


</script>

<style lang="scss">
$one: #bcc99c;
$two: #e1e89b;
$three: #a6b9a7;
$four: #74a0ad;
$gray: #cfd8dd;
$white: #f4f4f4;
$black: #262626;

body {
  background-color: $white;
  margin: 0;
  font-family: Arial, Arial, Helvetica, sans-serif;
  font-size: 14px;
  overflow: hidden;
}
input {
  border: none;

  &:focus {
    outline: none;
  }
}
.icon img {
  cursor: pointer;
}
h2  {
  margin: 10px 0;
}


.container {
  width: 100%;
  height: 100%;
  display: inline-grid;
  grid-template: 1fr / 1fr 4.6fr;
  .menu {
  
   grid-area: 1 / 1 / 1;
   background: $four;
   padding: 10px;
    -webkit-box-shadow: 1px 0px 8px 1px $gray;
    -moz-box-shadow: 1px 0px 8px 1px $gray;
    box-shadow: 1px 0px 8px 1px $gray;
   .page-title {
   display: flex;
   gap: 3px;
   align-items: center;
   justify-content: center;
   img {
    height: 2rem;
    width: 2rem;
    cursor: pointer;
    &:hover {
        opacity: 0.8;
      }
   }
   h1 {
    color: $white;
    font-size: 1.2rem;
    font-weight: 300;
    cursor: pointer;
    &:hover {
        opacity: 0.8;
      }
    }
  }
  .user-menu  {
    margin-top: 3rem;
    margin-left: 0.4rem;
  .item {
     display: flex;
     align-items: center;
     padding: 5px;
     font-size: 0.9rem;
     color: $white;
     gap: 4px;
    cursor: pointer;
    &:hover {
        opacity: 0.8;
      }
     img {
      height: 1.3 rem;
      }
     }
    }
     .app-menu  {
      margin-top: 3rem;
      margin-left: 0.7rem;
     .item {
      cursor: pointer;
      &:hover {
          opacity: 0.8;
        }
     display: flex;
    align-items: center;
     padding: 5px;
     font-size: 0.9rem;
     color: $white;
     gap: 7px;
     font-weight: 600;
     letter-spacing: 0.1rem;
     img {
      height: 1.3 rem;
      }
     }
    }
  }
  .dash-container {
    grid-area: 1 / 2 / 1;
    display: inline-grid;
    grid-template: 1fr 1.6fr 8fr / 1fr;
    
    .up-menu {
      padding: 0px 20px;
      grid-row: 1 / 2;
      grid-column: 1 / 3;
      height: 70px;
      display:flex;
      align-items: center;
      flex-wrap: wrap;
      .search {
        display: flex;
        gap: 10px;
        .icon {
          cursor: pointer;
          &:hover {
              opacity: 0.8;
            }
        }
        .bar input{
          width: 200px;
          background-color: $three;
          padding: 4px 10px; 
          color: $white;
          border-radius: 20px;
        }

      }
      .user-menu {
        margin-left: auto;
        align-items:center;
        display: flex;
        gap: 17px;
        flex-wrap: wrap;
        .notification {
          cursor: pointer;
          &:hover {
              opacity: 0.8;
            }
        }
        .user-profile {

          display: flex;
          align-items: center;
          gap: 7px;
          .user-icon {
          img {
          width: 50px;
          height: 50px;
          border-radius: 50px;
          cursor: pointer;
          &:hover {
              opacity: 0.8;
            }
          }
        }
          .user-full-name {
            font-size: 1rem;
            font-weight: 600;
            color: $black;
            padding: 0px 13px;
            cursor: pointer;
            &:hover {
                opacity: 0.8;
              }
        }
        }
        
      }

    }
    .lower-menu {
      padding: 10px 20px;
      grid-row: 2 / 3;
      grid-column: 1 / 3;
      display: flex;
      height: auto;
      align-items: center;
      div:last-child { 
        margin-left: auto;
      }
      .user {
        display: inline-grid;
        grid-template: 1fr 1fr 1fr / 1fr 3fr;
      .user-icon {
          grid-area: 1 / 1 / 4 / 6;
          img {
            height: 80px;
            width: 80px;
            border-radius: 50px;
            cursor: pointer;
            &:hover {
                opacity: 0.8;
              }
            
          }
        }
      .welcome-message {
          grid-area: 2 / 2 / 4 / 6;
      }
      .name {
          grid-area: 3 / 2 / 4 / 6;
          font-size: 1.3rem;
          font-weight: 600;
          color: $four;
          margin-top: -10px;
      }
      }
      .post-buttons {
        display: flex;
        gap: 10px;
      button {
        border: none;
        background-color: $two;
        padding: 7px 15px;
        border-radius: 20px;
        cursor: pointer;
        &:hover {
            opacity: 0.8;
          }
        text-transform: lowercase;
        color: $black;
        font-weight: bold;
      }
    }
    }
    .dashboard {
      padding: 10px;
      grid-row: 3 / 5;
      grid-column: 1 / 3;
      display: inline-grid;
      grid-template: 40vh 25vh / 70% 30%;
      background-color: $gray;
      box-shadow: inset 0 4px 2px -4px gray;
      h2 {
          font-size: 1.3rem;
          font-weight: normal;
          color: #607161;
        }
    .projects {
      width: 100%;
      grid-area: 1 / 1 / 3 / 2;
      .container {
       display: flex;
       gap: 10px;
       flex-wrap: wrap;
       width: 90%;
       margin: 0 auto;
       overflow: scroll;
       justify-content: center;
       align-items: center;
      .item {
        width: 200px;
        border-radius: 15px;
        padding: 10px;
        background-color: $white;
        border-left-color: $two;
        border-left-width: 5px;
        border-left-style: solid;
        box-shadow: 1px 2px 2px 1px rgba(87, 87, 87, 0.161);
        .project-info {
          
          h3 {
            color: $four;
            cursor: pointer;
            &:hover {
                opacity: 0.8;
              }
          }
          .summary {
            color: $black;
            text-align: justify;
            padding-left: 5px;
          }
        }
        .project-menu {
          display: flex;
          gap: 4px;
          justify-content: right;
          padding: 15px 5px;
          cursor: pointer;
          div:hover {
              opacity: 0.4;
            }
        }

      }
    }
    }
    .announce {
      grid-area: 1 / 2 / 2 / 3;
      .ann-container {
        overflow: scroll;
        padding:10px 15px;
        background-color: $white;
        text-align: center;
        border-radius: 10px;
        max-height: 210px;
        box-shadow: 1px 2px 2px 1px rgba(87, 87, 87, 0.161);
        .item {
          padding-top: 5px;
          width: 100%;
          margin: 0 auto;
          padding-bottom: 5px;
          border-bottom: 1px solid $gray;
        h4 {
          font-size: 0.9rem;
          margin:0px;
          color: #617362;
          text-align: left;
          cursor: pointer;
          &:hover {
              opacity: 0.8;
            }
        }
        .text {
          font-size: 0.7rem;
          text-align: left;
          color: $black
        }

        }

      }
    }
    .trend {
      grid-area: 2 / 2 / 3 / 2;
      .trend-container {
          overflow: scroll;
          padding: 10px 15px;
          background-color: $white;
          text-align: center;
          border-radius: 10px;
          height: 150px;
          box-shadow: 1px 2px 2px 1px rgba(87, 87, 87, 0.161);
          .item {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 4px 0px;
            .icon {
              img {
                width: 40px;
                height: 40px;
                border-radius: 50px;
                &:hover {
                    opacity: 0.8;
                  }
              }
            }
            .name {
              height:30px;
                h4 {
                  color: $three;
                  margin: 0px ;
                  cursor: pointer;
                  &:hover {
                      opacity: 0.8;
                    }
                  
                }
                p {
                  margin-top: -3px;
                  color: $black;
                }
              }
          }
      }
    }
  }
  }
}
</style>
