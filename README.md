# A-frame

# Start

## My set up

[KITSANAPONG WARIT / SE-A-Frame · GitLab](https://gitlab.com/6431503002/SE-A-Frame)

## Download

zip 

หรือ

`git clone [https://gitlab.com/6431503002/SE-A-Frame](https://gitlab.com/6431503002/SE-A-Frame)`

## Set up

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled.png)

`npm install`

สำคัญ อย่าข้าม 

เช็คด้วย พิมพ์ command ถูกที่รึเปล่า?

## Run

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled%201.png)

`npm start`

หรือ

กดที่ไฟล์ Run.bat (สำหรับ windows)

## อธิบาย Code

### <head>

```html
  <head>
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-particle-system-component@1.0.x/dist/aframe-particle-system-component.min.js"></script>
    <script src="https://unpkg.com/aframe-extras.ocean@%5E3.5.x/dist/aframe-extras.ocean.min.js"></script>
    <script src="https://unpkg.com/aframe-gradient-sky@1.0.4/dist/gradientsky.min.js"></script>
  </head>
```

เรียกใช้ A-frame

### <a-scene>

```html
<a-scene>
.....
</a-scene>
```

set ฉาก

### <a-assets>

```html
<a-assets>

      <img id="sky" src="assets/skybox/sunrise_panorama_7112.jpg">
      <a-asset-item id="girl" src="assets/just_a_girl/scene.gltf"></a-asset-item>
      <a-asset-item id="puente" src="assets/puente/scene.gltf"></a-asset-item>
      
    </a-assets> <!-- End assets -->
```

ของประกอบ ฉาก มีอะไรบ้าง

สิ่งที่อยู่ใน <a-assets> … </a-assets>

คิดสะว่าคือการประกาศตัวแปร 

<ชนิด id=”ชื่อ” src=”ไฟล์อยู่ไส?” >

### <body>

```html
<body>
  <a-scene>
				set ฉาก

    <a-assets>
	      ของประกอบ ฉาก
    </a-assets>

    <a-sky src="#sky"></a-sky>  ของทีใช้

    <a-entity gltf-model="#girl" id="updateMe" position="0 0 -8.45236" scale="0.03118 0.03118 0.03118"></a-entity> ของทีใช้

    <a-entity id="updateForWho" position="-0.2804 -0.00871 -4" rotation="0.33174256338074665 -1.8397674801650734 -0.010886198107485642"> ของทีใช้
      <a-camera></a-camera>
    </a-entity>

  </a-scene>

</body>
```

<ใช้ทำไร?   src=” #ของประกอบอันไหน? ”>   …. </ใช้ทำไร?>

### <a-sky>

[https://aframe.io/docs/1.3.0/primitives/a-sky.html](https://aframe.io/docs/1.3.0/primitives/a-sky.html)

The sky primitive adds a background color or 360° image to a scene. A sky is a large sphere with a color or texture mapped to the inside.

An equirectangular image as a background:

```html
<a-scene>
  <a-assets>
    <img id="sky" src="sky.png">
  </a-assets>
  <a-sky src="#sky"></a-sky>
</a-scene>
```

---

[Sky](https://www.notion.so/afe6591970c94d1bb7a7401906862d75)

### <a-entity gltf-model="#name">

[https://aframe.io/docs/1.3.0/components/gltf-model.html](https://aframe.io/docs/1.3.0/components/gltf-model.html)

Load a glTF model by pointing to an asset that specifies the **`src`** for a glTF file.

glTF = glb

```html
<a-scene>
  <a-assets>
    <a-asset-item id="tree" src="/path/to/tree.gltf"></a-asset-item>
  </a-assets>

  <a-entity gltf-model="#tree"></a-entity>
</a-scene>
```

---

## Tools

### **A-Frame Inspector**

[Visual Inspector & Dev Tools - A-Frame](https://aframe.io/docs/1.3.0/introduction/visual-inspector-and-dev-tools.html#a-frame-inspector)

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled%202.png)

**`<ctrl> + <alt> + i`** 

เปิด ****Inspector ช่วยจัดฉาก****

### ****A-Frame Watcher****

[https://github.com/supermedium/aframe-watcher](https://github.com/supermedium/aframe-watcher)

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled%203.png)

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled%204.png)

`aframe-watcher`

ช่วย save ฉากที่ใช้ ****Inspector จัด****

และโปรดตั้ง id ให้กับ entity ทุกตัว ไม่งั้นมันไม่เซฟ และ อย่าตั้งซ้ำ

```html
<a-entity gltf-model="#girl" id="updateMe" position="0 0 -8.45236" scale="0.03118 0.03118 0.03118"></a-entity>
```

![Untitled](A-frame%20fed4202803a744378d6403170334ca1a/Untitled%205.png)

อย่าลืม `y` เพื่อ save ด้วย
