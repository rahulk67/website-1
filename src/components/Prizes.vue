<template>
  <section class="prizes">
    <h1 class="section-title">Prizes</h1>
    <div class="prize__container">
      <div class="prize__note">
        Winning a prize in one category <strong>does not</strong> exclude you from winning a prize in another!
      </div>
      <ul class="prize__list">
        <li class="prize" v-for="prize in prizes">
          <img :src="imgPath(prize.image)" class="prize__image"></img>
          <h5 class="prize-category" v-html="prize.category"></h5>
          <h5 class="prize-amount" v-html="prize.amount"></h5>
        </li>
      </ul>
    </div>
    </section>
</template>

<script>
export default {
  name: 'Prize',
  props: ['prizes'],
  methods: {
    imgPath: function(imgName) {
      return require('@/assets/' + imgName)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url("https://fonts.googleapis.com/css?family=Quicksand:700");
@import url("https://fonts.googleapis.com/css?family=Nunito");

.prizes {
  width: 100%;
}

.section-title {
  font-family: 'Quicksand', sans-serif;
  font-size: 2.5vw;
  margin: 0 auto;
  color: #ff7bac;
  text-align: center;
  margin-bottom: 1.2vw;
  background: white;
  border-radius: 5vw;
  width: 15%;
}

.prize__container {
  font-family: 'Nunito', sans-serif;
  background-color: #ffebf1;
  box-shadow: 0 1.2vw #ffa6c7;
  border-radius: 6vw;
  padding: 2.5vw 2.2vw;
}

.prize__list {
  list-style: none;
  margin: 0;
  padding: 0;
  text-align: center;
  display: flex;
  justify-content: space-around;
}

.prize__note {
  font-size: 1vw;
  margin-bottom: 3vw;
  text-align: center;
}

.prize {
  width: 16.5vw;
  display: inline-block;
  vertical-align: top;
}

.prize__image {
  height: 4.5vw;
  width: 4.5vw;
  margin: auto;
}

.prize-category {
  text-align: center;
  color: black;
  margin: 1vw 0;
  font-size: 1.7vw;
}

.prize-amount {
  text-align: center;
  color: black;
  font-weight: normal;
  margin: 0.6vw 0;
  font-size: 1vw;
}

@media only screen and (min-device-width : 320px) and (max-device-width : 480px) {
  .prizes {
    margin: 0 auto;
    width: 90%;
  }

  .section-title {
    margin-bottom: 0.5rem;
    font-size: 2rem;
    width: 30%;
  }

  .prize__container {
    box-shadow: 0 0.8rem #ffa6c7;
    border-radius: 4rem;
    padding: 2rem 1rem;
  }

  .prize__list {
    display: block;
  }

  .prize__note {
    font-size: 1rem;
    margin-bottom: 3rem;
    text-align: center;
  }

  .prize {
    width: 49%;
    margin: auto;
  }

  .prize__image {
    height: 80px;
    width: 80px;
  }

  .prize-category {
    font-size: 1.1rem;
    margin: 0.5rem 0;
  }

  .prize-amount {
    font-size: 1.1rem;
    margin: 0;
    margin-bottom: 1.5rem;
  }
}

@media only screen and (min-device-width:768px) and (max-device-width:800px) {
  .prizes {
    margin: 2rem auto;
    width: 90%;
  }

  .section-title {
    font-size: 3.5rem;
    margin-bottom: 0.5rem;
    width: 30%;
  }

  .prize__container {
    border-radius: 6rem;
    padding: 5rem 1rem;
    box-shadow: 0 1.2rem #ffa6c7;
  }

  .prize__list {
    display: block;
  }

  .prize__note {
    font-size: 1.8rem;
    margin-bottom: 3vw;
    text-align: center;
  }

  .prize {
    width: 50%;
    margin: auto;
  }

  .prize__image {
    height: 200px;
    width: 200px;
  }

  .prize-category {
    font-size: 2rem;
    margin: 1rem 0;
    margin-bottom: 0;
  }

  .prize-amount {
    font-size: 2rem;
    margin: 2rem 0;
  }
}
</style>
