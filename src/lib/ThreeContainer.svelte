<script lang="ts">
    import * as Aframe from "aframe";
    
    const Boulder1Obj = new URL('../assets/Boulder1Obj.obj', import.meta.url).href;
    const Boulder1mtl = new URL('../assets/boulder1mtl.mtl', import.meta.url).href;
    const Boulder1Map = new URL('../assets/boulder1Map.jpg', import.meta.url).href;

</script>

<div class="h-[36vh]  w-[80vw] lg:h-[39vw] lg:w-[39vw]">
    <a-scene embedded vr-mode-ui="enabled: false">
        <a-camera position="0 0 1" look-controls="enabled: false" fov="50" />
        <a-assets>
            <a-asset-item id="boulder-obj" src={Boulder1Obj}></a-asset-item>
            <a-asset-item id="boulder-mtl" src={Boulder1mtl}></a-asset-item>
            <a-asset-item id="boulder-map" src={Boulder1Map}></a-asset-item>
        </a-assets>

        <a-obj-model animation="property: rotation; to: 0 360 0; loop: true; dur: 20000" src="#boulder-obj" mtl="#boulder-mtl" position="0 -5 -17"></a-obj-model>
    </a-scene>
</div>
