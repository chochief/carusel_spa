<template lang="pug">
  .slider(
    id="slider"
    @mousedown="startDrag"
    @mousemove="doDrag"
    @mouseup="stopDrag"
  )
    ul(
      id="sliderWrap"
      :style="sliderStyle"
    )
      li(
        v-for="slide in slides"
        :style="slideStyle"
      )
    div(id="prev" @click="prevSlider") &#8810
    div(id="next" @click="nextSlider") &#8811
</template>

<script>
export default {
  data () {
    return {
      sliderWidth: 0,
      slideWidth: 0,
      count: 1,
      offset: 0,
      slides: [
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' }
      ],
      sliderStyle: {
        left: '0px'
      },
      slideStyle: {
        width: '0px'
      },
      dragging: false,
      x: 'no',
      y: 'no',
      left: 0
    }
  },
  methods: {
    getSliderWidth () {
      const slider = document.getElementById('slider')
      this.sliderWidth = slider.offsetWidth
      this.slideWidth = slider.offsetWidth / 3 + 1
      this.slideStyle.width = `${this.slideWidth}px`
    },
    prevSlider () {
      if (this.count > 1) {
        this.count = this.count - 2
      } else {
        this.count = this.items - 1 - 2
      }
      this.offset = -(this.count * this.slideWidth)
      this.sliderStyle.left = `${this.offset}px`
      this.count++
    },
    nextSlider () {
      if (this.count < this.items - 2) {
        this.offset = -(this.count * this.slideWidth)
        this.sliderStyle.left = `${this.offset}px`
        this.count++
      } else {
        this.offset = 0
        this.sliderStyle.left = `${this.offset}px`
        this.count = 1
      }
    },
    startDrag (e) {
      this.dragging = true
      this.left = e.clientX
      console.log(this.x)
      // this.y = 0
    },
    doDrag (e) {
      if (this.dragging) {
        // let diff = this.x - e.clientX
        let diff = this.left - e.clientX
        // if (diff > 0) {
        //   this.nextSlider()
        // } else {
        //   this.prevSlider()
        // }
        // emit('mousestop')
        console.log(e.clientX, diff)
        this.sliderStyle.left = `-${diff}px`
        // this.sliderStyle.left = `-${this.x - e.clientX}px`
        // // this.x = e.clientX
        // let diff = this.x - e.clientX
        // // this.y = e.clientY
        // let sum = this.offset + diff * 10
        // this.x = e.clientX
        // // console.log(this.x, sum)
        // this.sliderStyle.left = `-${sum}px`
        // // this.sliderStyle.left = `-${this.count * this.sliderWidth + diff}px`
      }
    },
    stopDrag () {
      this.dragging = false
      this.x = 0
      // this.x = 'no'
      // this.y = 'no'
      console.log('this.dragging', this.x)
    }
  },
  computed: {
    items () {
      return this.slides.length
    }
  },
  mounted () {
    window.addEventListener('resize', this.getSliderWidth)
    this.getSliderWidth()
    window.addEventListener('mouseup', this.stopDrag)
  }
}
</script>

<style lang="scss" scoped>
$color1: cornflowerblue;
$color2: cadetblue;
$color3: bisque;
$color4: coral;
$color5: gold;
$color6: deeppink;

.slider {
  position: relative;
  z-index: 1;
  height: 250px;
  overflow: hidden;
  box-shadow: 0 0 3px rgba(0,0,0,0.3);
  margin: 60px 10px;
  border-radius: 4px;
}

ul {
  position: relative;
  z-index: 1;
  list-style: none;
  height: 100%;
  width: 9999%;
  padding: 0;
  margin: 0;
  // transition: all 750ms ease;
  left: 0;
  font-size: 0;

  li {
    position: relative;
    z-index: 1;
    height: 100%;
    // width: 80vw;
    float: left;
    font-size: 0;

    &:nth-child(1) {
      background-color: $color1;
    }
    &:nth-child(2) {
      background-color: $color2;
    }
    &:nth-child(3) {
      background-color: $color3;
    }
    &:nth-child(4) {
      background-color: $color4;
    }
    &:nth-child(5) {
      background-color: $color5;
    }
    &:nth-child(6) {
      background-color: $color6;
    }
  }
}

#prev, #next {
  width: 50px;
  line-height: 50px;
  border-radius: 50%;
  font-size: 21px;
  text-shadow: 0 0 20px rgba(0,0,0,0.6);
  text-align: center;
  color: white;
  text-decoration: none;
  position: absolute;
  z-index: 1;
  top: 50%;
  transform: translateY(-50%);
  transition: all 150ms ease;
  cursor: pointer;

  &:hover {
    background-color: rgba(0,0,0,0.1);
    text-shadow: 0;
  }
}

#prev {
  left: 10px;
}

#next {
  right: 10px;
}

</style>
