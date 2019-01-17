<template>
    <div>
        <Pixel isInColorPicker color="white" :current="color == 'white' ? true : false"/>
        <Pixel isInColorPicker color="silver" :current="color == 'silver' ? true : false"/>
        <Pixel isInColorPicker color="gray" :current="color == 'gray' ? true : false" />
        <Pixel isInColorPicker color="black" :current="color == 'black' ? true : false" />
        <Pixel isInColorPicker color="purple" :current="color == 'purple' ? true : false"/>
        <Pixel isInColorPicker color="fuchsia" :current="color == 'fuchsia' ? true : false" />
        <Pixel isInColorPicker color="maroon" :current="color == 'maroon' ? true : false" />
        <Pixel isInColorPicker color="red" :current="color == 'red' ? true : false"/>
        <Pixel isInColorPicker color="orange" :current="color == 'orange' ? true : false" />
        <Pixel isInColorPicker color="yellow" :current="color == 'yellow' ? true : false" />
        <Pixel isInColorPicker color="lime" :current="color == 'lime' ? true : false"/>
        <Pixel isInColorPicker color="green" :current="color == 'green' ? true : false" />
        <Pixel isInColorPicker color="olive" :current="color == 'olive' ? true : false" />
        <Pixel isInColorPicker color="teal" :current="color == 'teal' ? true : false"/>
        <Pixel isInColorPicker color="aqua" :current="color == 'aqua' ? true : false" />
        <Pixel isInColorPicker color="blue" :current="color == 'blue' ? true : false" />
        <Pixel isInColorPicker color="navy" :current="color == 'navy' ? true : false" />
    </div>
</template>


<script>
import Pixel from './Pixel.vue'

export default {
    name: 'ColorPicker',
    props: {
        color: String
    },
    components: {
        Pixel
    }
}
</script>

