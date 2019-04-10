<!-- 网站首页 -->
<template>
  <b-container fluid>
    <b-container>
      <b-carousel id="carousel1" controls indicators :interval="3000">
        <div v-for="(carouselImg, index) in carouselImgs" :key="index">
          <a :href="carouselImg.href">
            <b-carousel-slide :img-src="carouselImg.img"> </b-carousel-slide>
          </a>
        </div>
      </b-carousel>
      <br />
      <b-card-group columns>
        <b-card
          title="Card title that wraps to a new line"
          img-src="https://placekitten.com/g/400/450"
          img-fluid
          img-alt="image"
          img-top
        >
          <p class="card-text">
            This is a wider card with supporting text below as a natural lead-in
            to additional content. This content is a little bit longer.
          </p>
        </b-card>
      </b-card-group>
    </b-container>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      carouselImgs: [
        {
          img: 'https://picsum.photos/1110/416/?image=1',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=2',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=3',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=4',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=5',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=6',
          href: '/'
        }
      ]
    }
  }
}
</script>
