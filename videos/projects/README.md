# Project Demo Videos

Add your optimized, muted, loopable MP4 (and optionally WEBM) files here.

Recommended naming (match `index.html`):
- content_automation_demo.mp4
- sentiment_recs_demo.mp4
- telecom_churn_demo.mp4
- noise_forecasting_demo.mp4
- asthma_risk_demo.mp4

Encoding suggestion (H.264 MP4):
ffmpeg -i INPUT.mov -vf "scale=1280:-2,fps=24" -an -c:v libx264 -profile:v main -pix_fmt yuv420p -crf 30 -movflags +faststart output.mp4

Optional WEBM (VP9):
ffmpeg -i INPUT.mov -vf "scale=1280:-2,fps=24" -an -c:v libvpx-vp9 -b:v 0 -crf 37 output.webm

Keep each file ideally <4 MB. Use a poster image already referenced in the HTML for quick first paint.
