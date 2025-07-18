# 图片优化指南

## 问题诊断
您的网站图片过大，导致每个访客产生异常多的请求：
- 当前图片总大小：~29MB
- 建议优化后：<3MB

## 优化工具推荐

### 1. 在线压缩工具
- **TinyPNG**: https://tinypng.com/
- **Squoosh**: https://squoosh.app/
- **CompressJPEG**: https://compressjpeg.com/

### 2. 批量优化工具
```bash
# 使用ImageOptim (Mac)
# 使用GIMP批量处理
# 使用Photoshop批量导出
```

## 具体优化目标

### 当前文件 → 目标大小
- gaotie.jpg (4.3MB) → 150KB
- dianping.jpg (4.0MB) → 150KB  
- shanghai-food.jpg (3.4MB) → 150KB
- wechat-pay.jpg (3.3MB) → 150KB
- SIM.jpg (2.9MB) → 150KB
- china-itineraries.jpg (2.8MB) → 150KB
- alipay.jpg (2.7MB) → 150KB
- shanghai.jpg (2.3MB) → 150KB
- apps.jpg (1.4MB) → 100KB
- best-time.jpg (968KB) → 100KB

## 优化步骤

1. **使用TinyPNG批量压缩**
   - 上传所有JPG文件
   - 下载压缩后的文件
   - 替换原文件

2. **添加图片懒加载**
   ```html
   <img src="placeholder.jpg" data-src="actual-image.jpg" loading="lazy" alt="描述">
   ```

3. **使用WebP格式**
   ```html
   <picture>
     <source srcset="image.webp" type="image/webp">
     <img src="image.jpg" alt="描述">
   </picture>
   ```

## 预期效果
- 图片大小减少90%
- 页面加载速度提升5-10倍
- 请求数从718个/访客降至50-100个/访客 