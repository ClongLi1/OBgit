<div style="display: flex; flex-wrap: wrap; justify-content: space-between;">
  <!-- 左侧栏 -->
  <div style="width: 48%; margin-bottom: 20px;">
    <!-- 使用时长统计 -->
    ```dataviewjs
    let ftMd = dv.Pages (""). File.Sort (t => t.cday)[0]
    Let total = parseInt ([new Date () - ftMd. Ctime] / (60*60*24*1000))
    Let totalDays = " 🌅我已使用 **Obsidian** "+total+" 天，"
    Let nofold = '!"misc/templates"'
    Let allFile = dv.Pages (nofold). File
    Let totalMd = "共创建 "+
        AllFile. Length+" 篇笔记"
    Let totalTag = allFile.Etags.Distinct (). Length+" 个标签"
    Dv.Paragraph (
        TotalDays+totalMd+"、"+totalTag+""
    )
    ```
    
    <!-- 贡献图 -->
    
    
    <!-- 天气信息 -->
    <div style=" width: 100%; height:100;overflow: hidden; margin-top: 10px;">
      <iframe src="https://widget.pkmer.cn/free/miniTianqi?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&select-theme=ta&theme=%E6%A0%B7%E5%BC%8F4&input-text=&theme-color=%2350F9FFFF&select-icon=durian" allow="fullscreen" style=" height: 200%; width: 200%;"></iframe>
    </div>
  </div>
  
  <!-- 右侧栏 -->
  <div style="width: 48%;">
    <!-- 时钟 -->
    <div style="width: 100%; height:220px;overflow: hidden; margin-bottom: 20px;">
      <iframe src="https://widget.pkmer.cn/free/ColorfulClock?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&font-color=%2300FFD0FF&ring-color-1=%2330F503FF&ring-color-2=%23FF2A87FF&ring-color-3=%230008FFFF&ring-color-4=%23FFEE00FF&lang=zh-cn" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe>
    </div>
    
    <!-- Obsidian logo 和欢迎语 -->
    <div style="display: flex; align-items: center; margin-bottom: 20px;">
      <img src="Obsidian logo.png" alt="Obsidian Logo" style="width: 230px; height: 320px; margin-right: 20px;">
      <div>
        <h2>✨ 欢迎来到我的黑曜石 Obsidian 知识库！ 🌟</h2>
        <p>🔥这里是我的个人数字花园，更是我精心打造的知识宝库。在这个库里，你可以发现各种各样的笔记，💗从工作中的项目规划、行业动态分析，到个人成长中的读书心得、技能学习总结，应有尽有。  🌱我将每一个灵感瞬间、每一次深入思考都记录在此，并通过黑曜石强大的双向链接功能，让这些知识相互交织，形成独一无二的知识网络。💡这个库不仅帮助我高效整理思绪、回顾过往经验，还能助力我快速找到解决问题的灵感。它见证了我一路以来的成长与进步，相信也会成为你探索知识、激发创意的好帮手。 🚀快来一起探索吧！✨</p>
      </div>
    </div>
    
    <!-- 时间进度条 -->
    <div style="width: 100%; height:180px;overflow: hidden;">
      <iframe src="https://widget.pkmer.cn/free/TimeProgressBar?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&theme-color=%232D997AFF&select-theme=Default&date-picker=946310400000" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe>
    </div>
  </div>
</div>