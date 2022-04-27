```vue
<template>
  <div>
    <a id="down_qr" href="#" style="display: none" />
    <button @click="onHandle">button to get image</button>
  </div>
</template>

<script>
import html2canvas from "html2canvas";
export default {
  name: "Screenshots",
  methods: {
    onHandle() {
      html2canvas(document.body, {
        ignoreElements: (element) => {
          if (element.nodeName === "NOSCRIPT") {
            return true;
          }
        },
      }).then((canvas) => {
        var imgURL = canvas.toDataURL("image/png");
        const img = document.createElement("image");
        img.src = imgURL;
        document.documentElement.appendChild(img);
        document.getElementById("down_qr").download = imgURL;
        document.getElementById("down_qr").href = imgURL;
        document.getElementById("down_qr").click();
      });
    },
  },
};
</script>
```

