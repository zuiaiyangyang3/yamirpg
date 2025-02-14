# yamirpg
yamirpg

这是一个yamirpg解决导出安卓解决黑屏的补丁包,
1.解决安卓黑屏问题(webgl.js)
2.退出自动存档时，阻止关闭窗口，等写入结束后自动关闭，提升存档安全性(main.js)
3.退出自动存档时，先写入缓存，备份旧存档，重命名缓存为存档名，提升安全性(data.js)
4.启动读取自动存档时，先读取目标文件，如果失败再读取备份文件(data.js)
5.保存读取脚本代码兼容MacOS系统(data.js)
6.去除部分安卓手机严格的控制台警告(0号纹理未绑定)(scene.js,filter.js)
7.减少显存的占用，提升稳定性(webgl.js,ui.js,printer.js,伤害数字.js,生命值条.js)
8.自动获取设备支持的最大纹理尺寸(PC:16384,Mobile:4096)，避免文字纹理过大而报错，提升稳定性，如果兼容移动平台，控制图像文件分辨率在4096x4096以内
9.可能注意:没用到图像纹理压缩，低配电脑上爆显存有可能,表现为黑屏崩溃吧,如果是像素游戏，纹理估计不大
上门的话 翻译为英文


This is a Yamirpg patch package for solving Android export black screen issues:

1. **Solve Android black screen problems (webgl.js)**  
   Fix black screen issues on Android devices by modifying the `webgl.js` file.

2. **Prevent window closure when auto-saving upon exit, wait until writing is complete before closing automatically to improve save safety (main.js)**  
   When exiting the game, prevent the window from closing immediately and wait until the save process completes to ensure data integrity.

3. **When auto-saving upon exit, write to cache first, back up the old save, then rename the cache to the save file name to enhance safety (data.js)**  
   During the exit process, prioritize writing data to a temporary cache, back up the old save file, and rename the cache to the final save file after completion.

4. **When loading the auto-save on startup, read the target file first; if it fails, load the backup file instead (data.js)**  
   On startup, attempt to load the main save file. If it fails, fallback to the backup save file.

5. **Ensure save/load script compatibility with MacOS systems (data.js)**  
   Adjust the save/load scripts to ensure they work seamlessly across MacOS systems.

6. **Remove strict console warnings on some Android devices (e.g., "0 texture not bound") (scene.js, filter.js)**  
   Suppress unnecessary console warnings related to unbound textures on certain Android devices.

7. **Reduce VRAM usage to improve stability (webgl.js, ui.js, printer.js, damage numbers.js, health bar.js)**  
   Optimize memory usage in various scripts to reduce VRAM consumption and improve overall stability.

8. **Automatically detect the maximum supported texture size for the device (PC: 16384, Mobile: 4096) to avoid errors caused by excessively large text textures and enhance stability**  
   Ensure that image resolutions are controlled within 4096x4096 for mobile platforms to avoid texture-related errors. For pixel art games, this should generally not be an issue due to smaller texture sizes.

9. **Possible Note:** Texture compression is not utilized, so low-end computers may experience VRAM overflow, potentially leading to black screens or crashes. This is less likely to occur in pixel art games with smaller textures.

---

**Translation Complete.**