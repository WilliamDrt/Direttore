# Themes

### Load Themes

[Ctrl] + [O]  to load a theme. Files with ".drt-theme" extension.

### Make New Theme

[Ctrl] + [T]  to bring up Theme Editor

![Alt text](/Images/Theme_Editor.png?raw=true "DrtFMng-Theme Editor")

Editor starts with all fields blank,. Click "Pull from DrtfMngrPreview" to load app's current Theme. Change one of the fields (maybe one of the colors?) and click "Push to DrtFMngPreview". DrtFMngPreview will refresh itself and you should be able to see the changes. You can also load a Theme from disk. Once you're happy with all changes, write a title for it, "General/Title" and save it to disk. The final file should be something like: "yourtitle.drt-theme".

### Categories - Colors - Bitmaps - & stuff

There are 10 categories in theme editor, I believe they're self explained, click on a field to read a little hint/help text at the bottom of the form.

There are 4 kind of fields:

1. Color. Omitting a Color = Black
2. Boolean (true/false). Omitting a Boolean = false
3. Integer or Single. Omitting a Integer = 0
4. Bitmap. Omitting a Bitmap = App Crash. **Do not omit bitmaps**

It's better not to omit anything.

### Logical Size & DPI

Logical size is the size that would be used if DPI was 100%. If your bitmaps are going to support all DPIs all the way up to DPI 400%, then you'll have to multiply logical size X 400% (size x4). 

For example logical size for the scrollbar button is 14x14. Supporting all the way up to 400% would be (14x4=56) 56x56. What happens if you choose a bitmap with size, let's say 40x40 ? Monitors with DPI 400% will show the button a little bit "soft". Nothing really visible in my opinion, but mathematically it's there.

The opposite problem: Having a 56x56 scrollbar button displayed in a 100% monitor. If the button art has a lot of details, it can look a little bit "rough". Maybe some jagged edges or/and other problems. Simpler art (basic shadows, contour, no textures) will not have a problem.

I am hopping to resolve those issues, with your help, during this beta.

### UI Elements & Logical Size Table

| UI Element       | Logical Size | Comments                                                     |
| ---------------- | ------------ | ------------------------------------------------------------ |
| Scrollbar Button | 14x14        | You provide the Horizontal Left button. App will generate Right/Up/Down |
| Scrollbar Tray   | 1x14         | Drawn at Width x 14 with "nearest neighbor" algorithm. You provide the Horizontal Tray. App will generate the Vertical |
| Scrollbar Thumb  | 1x14         | Drawn at Width x 14 with "nearest neighbor" algorithm. You provide the Horizontal Thumb. App will generate the Vertical |
| Buttons          | 22x22        |                                                              |
| Buttons Overlays | 18x18        |                                                              |

If you have any questions or/and ideas please start a new [issue](https://github.com/WilliamDrt/DrtFMngPreview/issues).

DrtFMngPreview with a (half done) white theme:

![Alt text](/Images/White-Theme.png?raw=true "White Theme")