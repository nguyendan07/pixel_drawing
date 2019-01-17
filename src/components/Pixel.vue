<template>
    <div @click="handleClick" :class="['pixel', color, current ? 'current' : '']"></div>
</template>


<script>
export default {
    name: 'Pixel',
    props: {
        color: String,
        current: Boolean,
        isInColorPicker: Boolean,
        isInCanvas: Boolean,
        index: Number
    },
    methods: {
      handleClick: function() {
        if(this.isInColorPicker) {
          this.$root.$emit('updateColor', this.color)
        }
        if(this.isInCanvas) {
          this.$root.$emit('clickedpixel', this.index)
        }
      }
    }
}
</script>


<style scoped>
.pixel {
    border: 1px solid lightgray;
    width: 30px;
    height: 30px;
    box-sizing: border-box;
}

.navy {
  background-color: rgb(0, 31, 63);
}
.blue {
  background-color: rgb(0, 116, 217);
}
.aqua {
  background-color: rgb(127, 219, 255);
}
.teal {
  background-color: rgb(57, 204, 204);
}
.olive {
  background-color: rgb(61, 153, 112);
}
.green {
  background-color: rgb(46, 204, 64);
}
.lime {
  background-color: rgb(1, 255, 112);
}
.yellow {
  background-color: rgb(255, 220, 0);
}
.orange {
  background-color: rgb(255, 133, 27);
}
.red {
  background-color: rgb(255, 65, 54);
}
.maroon {
  background-color: rgb(133, 20, 75);
}
.fuchsia {
  background-color: rgb(240, 18, 190);
}
.purple {
  background-color: rgb(177, 13, 201);
}
.black {
  background-color: rgb(17, 17, 17);
}
.gray {
  background-color: rgb(170, 170, 170);
}
.silver {
  background-color: rgb(221, 221, 221);
}
.white {
  background-color: white;
}

.pixel.current {
  border: 4px solid yellow;
}
</style>

