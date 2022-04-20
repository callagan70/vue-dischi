<template>
<div>
    <div id="header">
      <img src="../assets/spotify-logo.png" alt="" class="color">
    </div>

    <div id="catalogue_card">
        <div class="album">
        
          <div  v-for="(element, index) in catalogue" v-bind:key="index" class="card">
                <div>
                  <img v-bind:src="element.poster" alt="Poster">
                <div class="card_title">
                    {{element.title}}
                </div>
                </div>
      


                <div>
                  {{element.author}}
                  <br>
                  {{element.year}}
                </div>
          </div>

            <!-- <VirtualCard 
            v-for="(element, index) in catalogue"
            v-bind:key="index"
            
            /> -->
        </div>
    </div>
</div>
</template>

<script>
// import axios from 'axios';
// import VirtualCard from './VirtualCard.vue'

export default {
    name: 'HeaDer',
//  components: {
//     VirtualCard
//   },

  data(){
    return{
      catalogue: [
{
"poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
"title": "New Jersey",
"author": "Bon Jovi",
"genre": "Rock",
"year": "1988"
},
{
"poster": "https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg",
"title": "Live at Wembley 86",
"author": "Queen",
"genre": "Pop",
"year": "1992"
},
{
"poster": "https://images-na.ssl-images-amazon.com/images/I/41JD3CW65HL.jpg",
"title": "Ten's Summoner's Tales",
"author": "Sting",
"genre": "Pop",
"year": "1993"
},
{
"poster": "https://cdn2.jazztimes.com/2018/05/SteveGadd-800x723.jpg",
"title": "Steve Gadd Band",
"author": "Steve Gadd Band",
"genre": "Jazz",
"year": "2018"
},
{
"poster": "https://images-na.ssl-images-amazon.com/images/I/810nSIQOLiL._SY355_.jpg",
"title": "Brave new World",
"author": "Iron Maiden",
"genre": "Metal",
"year": "2000"
},
{
"poster": "https://upload.wikimedia.org/wikipedia/en/9/97/Eric_Clapton_OMCOMR.jpg",
"title": "One more car, one more raider",
"author": "Eric Clapton",
"genre": "Rock",
"year": "2002"
},
{
"poster": "https://images-na.ssl-images-amazon.com/images/I/51rggtPgmRL.jpg",
"title": "Made in Japan",
"author": "Deep Purple",
"genre": "Rock",
"year": "1972"
},
{
"poster": "https://images-na.ssl-images-amazon.com/images/I/81r3FVfNG3L._SY355_.jpg",
"title": "And Justice for All",
"author": "Metallica",
"genre": "Metal",
"year": "1988"
},
{
"poster": "https://img.discogs.com/KOBsqQwKiNKH-q927oHMyVdDzSo=/fit-in/596x596/filters:strip_icc():format(jpeg):mode_rgb():quality(90)/discogs-images/R-6406665-1418464475-6120.jpeg.jpg",
"title": "Hard Wired",
"author": "Dave Weckl",
"genre": "Jazz",
"year": "1994"
},
{
"poster": "https://m.media-amazon.com/images/I/71K9CbNZPsL._SS500_.jpg",
"title": "Bad",
"author": "Michael Jacjson",
"genre": "Pop",
"year": "1987"
}
]
    }
},

  // created(){
  //   axios.get( 'https://flynn.boolean.careers/exercises/api/array/music' )
  //        .then( ( response )=>{
  //          console.log( response);

  //          this.avatarsArray = response.data
  //        } )

  //        .catch( (error) => {
  //          console.log( error )
  //        } )
  // }
}
</script>


<style scoped lang="scss">

#header{
  width: 100%;
  background-color: #2E3A46;
  height: 5vh;
}

.color{
padding: 10px;
 width: 20px;
}

#catalogue_card{
height: 95vh;
background-color: #1E2D3B;
padding: 25px 0px 0px 0px;

    .album{
      width: 70vw;
      height: fit-content;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;

      .card{
        display: flex;
        width: calc((100%/5) - 20px);
        margin-top: 50px;
        text-align: center;
        height: 300px;
        background-color: #2E3A46;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
        // border: 1px solid red;

        .card_title{
          color: white;
          text-transform: uppercase;
          font-family: Arial, Helvetica, sans-serif;

        }
      }

      .card img{
        width: 75%;
        height: 75%;
        object-fit: cover;
        margin-bottom: 1em;
      }
    }
}



</style>
