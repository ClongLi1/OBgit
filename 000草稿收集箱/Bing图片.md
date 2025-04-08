```dataviewjs
// 获取当前日期
const currentDate = new Date();
const year = currentDate.getFullYear();
const month = String(currentDate.getMonth() + 1).padStart(2, '0');
const day = String(currentDate.getDate()).padStart(2, '0');
const formattedDate = `${year}${month}${day}`;

// Bing每日图片API
const bingApiUrl = `https://www.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1&mkt=en-US`;

// 获取图片信息
const fetchBingImage = async () => {
  try {
    const response = await dv.http.get(bingApiUrl);
    if (response && response.images && response.images.length > 0) {
      const image = response.images[0];
      const imageUrl = `https://www.bing.com${image.url}`;
      const imageTitle = image.title;
      const imageDescription = image.copyright;
      return { imageUrl, imageTitle, imageDescription };
    }
  } catch (error) {
    console.error('Error fetching Bing image:', error);
  }
  return null;
};

// 获取图片并生成Markdown内容
const generateMarkdown = async () => {
  const imageInfo = await fetchBingImage();
  if (imageInfo) {
    return `
# Daily Bing Image - ${currentDate.toLocaleDateString()}
![${imageInfo.imageTitle}](${imageInfo.imageUrl})

**Title:** ${imageInfo.imageTitle}

**Description:** ${imageInfo.imageDescription}
    `;
  }
  return 'Failed to load Bing image. Please try again later.';
};

// 显示内容
dv.header(1, `Bing Daily Image - ${currentDate.toLocaleDateString()}`);
dv.paragraph('Loading...');
dv.el('img', '', (img) => {
  img.style.width = '100%';
  img.style.maxWidth = '800px';
  img.style.height = 'auto';
  img.style.margin = '20px 0';
});

// 动态更新内容
const updateContent = async () => {
  const markdownContent = await generateMarkdown();
  dv.paragraph(markdownContent);
};

// 初始加载
updateContent();

// 每天自动更新
setInterval(() => {
  const now = new Date();
  if (now.getDate() !== currentDate.getDate()) {
    currentDate.setDate(now.getDate());
    updateContent();
  }
}, 3600000); // 每小时检查一次
```
