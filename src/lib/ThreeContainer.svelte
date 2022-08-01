<script lang="ts">
    import * as Aframe from "aframe";

    const BoulderPonderosa = new URL('../assets/BoulderPonderosa.gltf', import.meta.url).href;

    console.log(BoulderPonderosa.toString());

</script>

<div class="h-[36vh]  w-[80vw] lg:h-[39vw] lg:w-[39vw]">
    <a-scene embedded vr-mode-ui="enabled: false">
        <a-camera position="0 0 1" look-controls="enabled: false" wasd-controls-enabled="false" fov="50" />

        <a-entity light="type: directional; color: #FFF; intensity: 1.6" position="-0.5 1 1"></a-entity>
        <a-entity animation="property: rotation; to: 0 360 0; loop: true; dur: 20000" gltf-model={BoulderPonderosa} position="0 -3 -11"></a-entity>
    </a-scene>
</div>
