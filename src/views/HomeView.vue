<template>
  <div class="home">
    <div class="feature-card">
      <router-link to="/movies/tt4409">
        <img class="feature-image" src="../assets/prisonbreak.jpeg">
        <div class="detail">
          <h3>Prison Break</h3>
          <p>Prison Break is an American serial drama television series 
            created by Paul Scheuring for Fox. </p>
        </div>
      </router-link>
    </div>
    <form @submit.prevent class="search-box">
      <input type="text" placeholder="what are you looking for?">
      <input type="submit" value="search">
    </form>
    <div class="movie-list">MOVIES</div>
  </div>
</template>

<script>


export default {
 
 
}
</script>

<style lang="scss">
  .home{
    .feature-card{
      position: relative;

      .feature-image{
        display: block;
        width: 100%;
        height: 300px;
        object-fit: cover;
        position: relative;
        z-index: 0;
      }
      .detail{
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.6);
        padding: 16px;
        z-index: 1;

        h3{
          color: #FFF;
          margin-bottom: 16px;
        }

        p{
          color: #FFF;
        }
      }
    }
    .search-box{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 16px;

      input{
        display: block;
        appearance: none;
        outline: none;
        border: none;
        background: none;

        &[type='text']{
          width: 100%;
          color: #FFF;
          background-color: #496583;
          font-size: 20px;
          padding: 10px 16px;
          border-radius: 8px;
          margin-bottom: 16px;
          transition: 0.4s;

          &::placeholder{
            color: #f3f3f3;
          }
          &:focus{
            box-shadow: 0px 3px 6px rgba(0, 0, 0 , 0.2) ;
          }
        }
        &[type='submit']{
          widows: 100%;
          max-width: 300px;
          background-color: #42B883;
          padding: 16px;
          border-radius: 8px;
          color: #FFF;
          font-size: 20px;
          text-transform: uppercase;
          transition: 0.4s;

          &:active{
            background-color: #3B8070;
          }
        }
      }
    }
  }
</style>
