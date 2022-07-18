<script lang="ts">
    import * as Aframe from 'aframe';


</script>

<div class="relative w-[70vw] h-[30vh] lg:w-[30rem] lg:h-[30rem]">
    <a-scene embedded  vr-mode-ui="enabled: false">
        <a-camera look-controls="enabled: false"/>
        <a-box position="-1 0.5 -3"  rotation="0 45 0" color="#4CC3D9" width="0.2" height="0.2" depth="0.2"></a-box>
    </a-scene>
</div>
