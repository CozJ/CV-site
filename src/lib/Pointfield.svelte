<script lang="ts">
    import * as Aframe from 'aframe';


</script>

    <div class="h-[36vh]  w-[80vw] lg:h-[39vw] lg:w-[39vw]">
        <a-scene embedded vr-mode-ui="enabled: false">
            <a-camera position="0 0 1" look-controls="enabled: false" fov="50"/>
            <a-box animation="property: rotation; to: 0 -180 180; loop: true; dur: 5000;" position="0 0 -1"  rotation="0 0 0" color="#4CC3D9" width="0.1" height="0.1" depth="0.1"></a-box>
            <a-tetrahedron animation="property: rotation; to: 0 180 180; loop: true; dur: 5000;" position="0.3 0.2 -0.8"  rotation="0 0 0" color="#4CC3D9" radius="0.06"></a-tetrahedron>
            <a-torus animation="property: rotation; to: 0 180 180; loop: true; dur: 5000;" position="-0.3 -0.2 -0.8"  rotation="0 0 0" color="#4CC3D9" radius="0.06" radius-tubular="0.01" radius-ring="0.3"></a-torus>
        </a-scene>
    </div>

    
