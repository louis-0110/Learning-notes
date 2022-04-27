doc文档转html

 

```js
 <div v-html="docx"></div>
<input type="file" @input="getDocx" />
  
import { convertToHtml } from "mammoth";

 		axios
      .get("/1.docx", {
        responseType: "arraybuffer",
      })
      .then((res) => {
        this.renderDocx(res.data);
      })
      .catch((err) => {
        console.error(err);
      });

 getDocx(e) {
      e.target.files[0].arrayBuffer().then((res) => {
        this.renderDocx(res);
      });
    },
      

 renderDocx(data) {
      convertToHtml({ arrayBuffer: data })
        .then((result) => {
          this.docx = result.value; // The generated HTML
        })
        .done();
 },
```

