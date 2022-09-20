<script>
    import Card from "./Card.svelte";
    import {productos} from '../../../store/images';

    import { Swiper, SwiperSlide } from "swiper/svelte";

    // Import Swiper styles
    import "swiper/css";

    import "swiper/css/pagination";
    import "swiper/css/navigation";

    // import required modules
    import { Pagination, Navigation } from "swiper";
</script>

<section>
    
    <Swiper
        slidesPerView={3}
        spaceBetween={100}
        slidesPerGroup={3}
        loop={true}
        loopFillGroupWithBlank={false}
        pagination={{
            clickable: true,
        }}
        navigation={true}
        modules={[Pagination, Navigation]}
        class="mySwiper"
        breakpoints={{
            "300": {
              slidesPerView: 1,
              spaceBetween: 0,
            },
            "400": {
              slidesPerView: 2,
              spaceBetween: 0,
            },
            "500": {
              slidesPerView: 2,
              spaceBetween: 0,
            },
            "600": {
              slidesPerView: 2,
              spaceBetween: 10,
            },
            "768": {
              slidesPerView: 3,
              spaceBetween: 10,
            },
            "1024": {
              slidesPerView: 4,
              spaceBetween: 30,
            },
          }}
          centeredSlides={true}
          centeredSlidesBounds={true}
        >
        {#each productos as producto}
        <SwiperSlide>
            <Card name={producto.name} price={producto.price} image={producto.image}/>
        </SwiperSlide>
        {/each}

    </Swiper>   
    
</section>

<style>
    

    section{
        width: 90%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
    }



</style>