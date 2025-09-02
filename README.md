# Animefy My Photo | My Journey from Blurry Filters to GAN Magic

This repository is a story of how I went from a **failed cartoonizer attempt** (that made Tom Cruise look like a bad blur) to a **working anime-style GAN model** (that finally gave me a tiger image that looked straight out of a Ghibli frame).

It’s not just code — it’s my learning curve.

---

## 🌟 Why I Started

Turning your photos into anime/cartoon/Ghibli-style images was trending everywhere.  
I saw those filters online and thought: *why not build my own?*  

I wanted to:  
- Learn how OpenCV filters actually work under the hood  
- See why some images stylize well and others don’t  
- Push myself to try deep learning (GANs) after failing with classical methods  

---

## 🛠️ My First Attempt (v1)

**Notebook:** `01_cartoonizer_baseline.ipynb`  

I started simple with OpenCV:  
- Median blur → smooth the photo  
- Adaptive threshold → get edges  
- Bilateral filter → flatten colors  
- Combine them together  

I tested it on Tom Cruise’s photo and… well, it didn’t look like anime at all.  
- The face looked blurry  
- Edges were broken  
- Skin looked patchy  
- The background was distracting  

It was a good starting point, but honestly, the result felt more like a failed Snapchat filter.

---

## 🐅 Breakthrough with GAN (v2)

**Notebook:** `02_cartoonizer_gan.ipynb`  

That’s when I moved to a **GAN model (IPPR-GAN)**.  
This model doesn’t just “filter” the photo — it **learns the style** of anime/cartoon art.  

The steps:  
- Preprocess the image (resize + normalize)  
- Feed it into the GAN generator  
- Postprocess with a little sharpening for clear lines  

When I ran it on the tiger photo, it blew me away:  
- Flat color fills like anime cels  
- Bold outlines  
- Stylized look that actually *felt* like art  

This was the moment my project finally worked.  

---

## 🔍 Before vs After

### Tom Cruise
- v0 → Blurry, blotchy, not anime-like  
- v2 → Cleaner edges, stylized look (still tricky with portraits, but better)  

### Tiger
- v0 → Over-smoothed, unnatural  
- v2 → Convincing anime/cartoon style — this one finally made me smile  

*(Once I add the images in `samples/` and `results/`, I’ll embed them here with before/after screenshots.)*

---


---

## 🧠 What I Learned

- Blurs and thresholds can only go so far — they break on real photos  
- GANs learn style in a way that filters simply cannot  
- Portraits are much harder than high-contrast animals  
- Failure photos (like Tom Cruise) are just as valuable as success ones — they show progress  

---

## 🔁 My Journey in Short

- **v0:** Tried OpenCV filters → ended up with blotchy, cartoon-but-not-anime results  
- **v2:** Switched to GAN → tiger image finally looked like anime  

---

## 📜 License & Credits

- Code: MIT  
- Built with OpenCV + PyTorch (IPPR-GAN)  
- Thanks to the open-source community for all the tutorials that guided me along the way  
