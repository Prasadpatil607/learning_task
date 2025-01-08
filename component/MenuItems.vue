<template>
    <div class="container">
      <div class="carousel-wrapper">
        <div class="carousel-track" ref="track">
          <div v-for="(item, index) in carouselItems" :key="index" class="carousel-item">
            <div class="hoverbox">
              <img :src="item.image" :alt="item.title">
              <div class="hoverbox-content font-bold">
                <h3 v-html="item.title.replace(' ', '<br>')"></h3>
                <p>{{ item.description }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="carousel-nav">
          <button class="prev" @click="moveSlide(-1)">❮</button>
          <button class="next" @click="moveSlide(1)">❯</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed, onMounted, onUnmounted } from 'vue';
  
  interface CarouselItem {
    image: string;
    title: string;
    description: string;
  }
  
  const carouselItems: CarouselItem[] = [
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-delicious-dinner.png',
      title: 'Spicy Chicken Spaghetti',
      description: 'Served with green chillies'
    },
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/bread-bun-chopping-board.png',
      title: 'Smoked Beef Sub-Sandwich',
      description: 'Slow cooked beef sub'
    },
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/antioxidant-beverage-carrot-juice.png',
      title: 'Grilled Chicken Salad',
      description: 'Fresh and healthy'
    },
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/sec.jpg',
      title: 'Cold milk shake Juice',
      description: 'With fresh milk'
    },
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-calcium-cereal.png',
      title: 'Blueberry Smoothie',
      description: 'With fresh peppermint'
    },
    {
      image: 'https://themewagon.gitlab.io/restaurant/assets/img/food/antioxidant-beverage-carrot-juice.png',
      title: 'Spicy Chicken Spaghetti',
      description: 'Served with green chillies'
    }
  ];
  
  const currentIndex = ref(0);
  const itemWidth = 25; // Each item takes 25% of the container
  const maxIndex = computed(() => carouselItems.length - 4); // Maximum sliding index
  const track = ref<HTMLElement | null>(null);
  
  const moveSlide = (direction: number) => {
    currentIndex.value = Math.max(0, Math.min(currentIndex.value + direction, maxIndex.value));
    updateCarousel();
  };
  
  const updateCarousel = () => {
    if (track.value) {
      const offset = currentIndex.value * -itemWidth;
      track.value.style.transform = `translateX(${offset}%)`;
    }
  };
  
  // Auto-play functionality
  onMounted(() => {
    const autoPlayInterval = setInterval(() => {
      currentIndex.value = currentIndex.value >= maxIndex.value ? 0 : currentIndex.value + 1;
      updateCarousel();
    }, 5000);
  
    // Clean up interval on component unmount
    onUnmounted(() => {
      clearInterval(autoPlayInterval);
    });
  });
  </script>
  
  <style scoped>
  /* .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    position: relative;
  }
  
  .carousel-wrapper {
    position: relative;
    overflow: hidden;
  }
  
  .carousel-track {
    display: flex;
    gap: 20px;
    transition: transform 0.5s ease-in-out;
  }
  
  .carousel-item {
    flex: 0 0 calc((100% - 60px) / 4); 
    position: relative;
    aspect-ratio: 3/4;
  }
  
  .hoverbox {
            position: relative;
            height: 100%;
            border-radius: 10px;
            overflow: hidden;
  }
  
 
  
  .hoverbox:hover img {
    transform: scale(1.1);
  }
  
  .hoverbox-content {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
    color: white;
    padding: 20px;
    opacity: 0;
    transition: opacity 0.3s;
  }
  
  .hoverbox:hover .hoverbox-content {
    transform: translateY(0);
  }
  
  .hoverbox-content h3 {
    margin: 0 0 10px;
    font-size: 1.2em;
  }
  
  .hoverbox-content p {
    margin: 0;
    font-size: 0.9em;
  }
  
  .carousel-nav {
    position: absolute;
    top: 50%;
    left: 0;
    right: 0;
    transform: translateY(-50%);
    display: flex;
    justify-content: space-between;
    pointer-events: none;
  }
  
  .carousel-nav button {
    background: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 20px 15px;
    cursor: pointer;
    pointer-events: auto;
    transition: background-color 0.3s ease;
    border-radius: 4px;
  }
  
  .carousel-nav button:hover {
    background: rgba(0, 0, 0, 0.8);
  }
  
  .prev {
    margin-left: -50px;
  }
  
  .next {
    margin-right: -50px;
  } */


  
  .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }

        .carousel-wrapper {
            position: relative;
            overflow: hidden;
        }

        .carousel-track {
            display: flex;
            gap: 20px;
            transition: transform 0.5s ease-in-out;
        }

        .carousel-item {
            flex: 0 0 calc((100% - 60px) / 4); /* 4 items with 20px gap */
            position: relative;
            aspect-ratio: 3/4;
        }

        .hoverbox {
            position: relative;
            height: 100%;
            border-radius: 10px;
            overflow: hidden;
        }

        .carousel-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10px;
        }

        .hoverbox-content {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
            color: white;
            padding: 20px;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .hoverbox:hover .hoverbox-content {
            opacity: 1;
        }

        .hoverbox-content h3 {
            font-size: 1.5rem;
            text-transform: uppercase;
            margin: 0;
            line-height: 1.3;
        }

        .hoverbox-content p {
            margin-top: 5px;
            font-size: 0.9rem;
        }

        .carousel-nav {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 100%;
            left: 0;
            right: 0;
            z-index: 10;
            pointer-events: none;
        }

        .carousel-nav button {
            position: absolute;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: white;
            border: none;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            cursor: pointer;
            pointer-events: auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
        }

        .carousel-nav button:hover {
            background: #f78d03;
        }

        .carousel-nav .prev {
            
            opacity: 0.5;
            background-color: #f08c0993;
        }

        .carousel-nav .next {
            right: 0px;
            opacity: 0.5;
            background-color: #f08c0993;
        }
  </style>