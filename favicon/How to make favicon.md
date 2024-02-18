顏色來源:
- [Google Color palette](https://partnermarketinghub.withgoogle.com/brands/google-news/visual-identity/color-palette/)

參考文章:
- [Favicon Generator. For real.](https://realfavicongenerator.net/favicon_result?file_id=p1hmu1470b18211omkgm1eqv17c6)
- [認識 Favicon，並使用工具協助完整性](https://medium.com/unalai/%E8%AA%8D%E8%AD%98-favicon-%E4%B8%A6%E4%BD%BF%E7%94%A8%E5%B7%A5%E5%85%B7%E5%8D%94%E5%8A%A9%E5%AE%8C%E6%95%B4%E6%80%A7-f41658955657)

設計 png 流程
1. 開啟小畫家, 設定寬高為 192 px
1. 開始畫圖, 顏色從 Google Color palette 中挑選藍色 #4285F4 儲存為 192x192
1. 開啟檔案 192x192 調整寬高分別為 512x512, 48x48 分別另存新檔為 512x512, 48x48
1. 新增檔案, 檔名為 manifest.webmanifest.json 的檔案, 內容為
    ```JSON
    {
    "name": "大順國電器行",
    "icons": [
        { "src": "favicon-192.png", "type": "image/png", "sizes": "192x192" },
        { "src": "favicon-512.png", "type": "image/png", "sizes": "512x512" }
    ]
    }
    ```

設計 apple touch icon 流程
1. 開啟小畫家, 設定寬高 140
1. 開始畫圖, 顏色從 Google Color palette 中挑選藍色 #4285F4
1. 將畫布寬高拉大為 180
1. 另存新檔為 apple-touch-icon.png

設計 ico 流程
1. 開啟 GIMP 2, 開啟檔案 148x48, 另存新檔為 favicon.ico, 設定為 32bpp, 8-bit Alpha, no palette

設計 svg 流程 (跳過, 因為這個方法產生的 svg 會取代 favicon.ico 而且底層不是透明的, 所以最後沒採用)
1. 開啟 PowerPoint, 設定投影片大小為 1英寸
1. 開始畫圖, 顏色從 Google Color palette 中挑選藍色 #4285F4
1. 另存新檔為 icon.svg

成果
```HTML
    <!-- title -->
    <title>大順國電器行</title>

    <!-- favicon -->
    <link rel="icon" href="favicon.ico" sizes="any">
    <link rel="icon" href="icon.svg" type="image/svg+xml">
    <link rel="apple-touch-icon" href="apple-touch-icon.png">
    <link rel="manifest" href="manifest.webmanifest">
```

發現 icon.svg 會取代 favicon.ico 而且底層不是透明的, 最後不採用, 所以實際上使用
```HTML
    <!-- title -->
    <title>大順國電器行</title>

    <!-- favicon -->
    <link rel="icon" href="favicon.ico" sizes="any">
    <link rel="apple-touch-icon" href="apple-touch-icon.png">
    <link rel="manifest" href="manifest.webmanifest">
```
