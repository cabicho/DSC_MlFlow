# DSC_MlFlow



Using a relative or absolute URL (from the web or a local path):
    ![Alt text for the image](image_url_or_path "Optional title for the image")
    ![Alt text for the image]("DSC_MlFlow/pdf/img/01/1. Objectivos de MlOps.png" "Optional title for the image") 

    ![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png "GitHub Octocat")
    ![GitHub Logo](DSC_MlFlow/pdf/img/01/'1. Objectivos de MlOps.png' "GitHub Octocat")
    ![GitHub Logo]('DSC_MlFlow/pdf/img/01/1. Objectivos de MlOps.png' "GitHub Octocat")
    ![GitHub Logo]("DSC_MlFlow/pdf/img/01/1. Objectivos de MlOps.png" "GitHub Octocat")

Image from a relative path in your repository:
    ![Screenshot of the application](assets/screenshot.png)
    ![Screenshot of the application](DSC_MlFlow/pdf/img/01/1.Objectivos-de-MlOps.png)


Using an HTML <img> tag (for more control):
    <img src="DSC_MlFlow/pdf/img/01/1.Objectivos-de-MlOps.png" alt="Alt text for the image" width="500" height="300" align="center">

    <img src="https://example.com/my-awesome-graphic.gif" alt="My Awesome Graphic" width="600">



how can i insert video in readme.md
    1. The "Clickable Thumbnail" Method (Most Common and Recommended)
    This is the most widely supported and effective method. You combine Markdown's image and link syntax to create a clickable image (a thumbnail) that, when clicked, opens the video in a new tab.
    Concept: [![Alt text for image](path/to/thumbnail.jpg)](URL_of_your_video "Optional title for video link")Create or find a video thumbnail:

For YouTube/Vimeo: These platforms often provide default thumbnails. For YouTube, you can often get a thumbnail like this: https://img.youtube.com/vi/VIDEO_ID/maxresdefault.jpg (replace VIDEO_ID with the actual ID from the YouTube URL). You can also try 0.jpg, 1.jpg, hqdefault.jpg, etc., for different qualities.

For other hosted videos or local videos: Take a screenshot of a good frame from your video and save it as an image (e.g., thumbnail.png or thumbnail.jpg). Place this image in your repository (e.g., in an assets folder).
Construct the Markdown:
[![Watch the video](https://img.youtube.com/vi/dQw4w9WgXcQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=dQw4w9WgXcQ "Click to watch the video demo")
Replace dQw4w9WgXcQ with your YouTube video ID.

If using a local thumbnail:
[![Project Demo](assets/demo_thumbnail.png)](https://example.com/path/to/your/video.mp4 "View Project Demo")
Advantages:

Works across almost all Markdown renderers.

Doesn't embed a heavy video directly, keeping your README.md lightweight.

Provides a visual cue to the user.
    2. Using HTML <video> tag (Limited Support, but possible on GitHub)
    While Markdown doesn't natively support video tags, many Markdown renderers (including GitHub's) will parse raw HTML. This gives you more control, but it's not universally supported.
        <video src="URL_of_your_video.mp4" controls width="640" height="360" poster="optional_thumbnail.jpg"></video>
        <video src="assets/demo.mp4" controls width="700"></video>
        <video src="https://github.com/YOUR_USERNAME/YOUR_REPO/assets/YOUR_ASSET_ID/YOUR_VIDEO_GUID.mp4" controls width="600"></video>
Explanation of attributes:

src: The URL to your video file. This can be a relative path if the video is in your repository (e.g., assets/my_video.mp4) or an external URL.

controls: Adds default video controls (play/pause, volume, fullscreen). Highly recommended.

width, height: Sets the dimensions of the video player in pixels.

autoplay: (Use with caution) Makes the video start playing automatically. Many browsers block autoplay with sound unless the user interacts first.

loop: Makes the video loop continuously.

muted: Mutes the video by default. Often used with autoplay.

poster: Specifies an image to be displayed while the video is downloading, or until the user hits the play button. This acts as a static preview.
Example for a video hosted in your GitHub repository:

If your video demo.mp4 is in an assets folder:
<video src="assets/demo.mp4" controls width="700"></video>
Advantages:

Provides a native video player experience directly in the README.md.

More control over player behavior (autoplay, loop, controls).

Disadvantages:

Not all Markdown renderers support raw HTML, so it might not work everywhere.

Directly embedding large video files can make your repository larger and slow down loading for users.
    3. Converting to an Animated GIF (for short, small demos)
For very short, silent demonstrations, converting your video to an animated GIF can be a good option. GIFs are treated like images in Markdown.

Steps:

Convert your video (e.g., MP4) to a GIF using an online converter or software like FFmpeg.

Optimize the GIF for file size.

Insert it like a regular image:  
        ![Short Demo GIF](assets/short_demo.gif)