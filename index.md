# STATS 220 ASSIGNMENT 1
## My Time Management Issues
![](rip_meme.png)

## My Motivation Behind the Meme
For the first time in my life, I could say that looking up memes on reddit was for *"research purposes"*. I wanted to create a generally relatable meme that wasn't targeted to a specific group of people. I thought of creating a data science meme, but I just couldn't come up with something genuinely funny or relatable, so I decided to project my *master procrastination skills* onto my meme. After hours of research and debating, this was the result. Although not a difficult meme to create code-wise, I wanted the person looking at the meme to think, "hey, that's so me," or "hey, that's pretty funny." Hopefully I have achieved my goals.

### SOURCE CODE:
```r
library(magick)
#Images found from Google, then edited and cropped in photoshop.
image_1 <- image_read("image1.png") %>%
  image_scale("x300") %>% image_border("#000000", "4x4") %>%
  image_annotate("Tutorials", size = 20, color = "white", boxcolor = "black",
                 location = "+70+40", font = "Impact") %>%
  image_annotate("Assignments", size = 20, color = "white", boxcolor = "black",
                 location = "+380+60", font = "Impact") %>%
  image_annotate("Midterms", size = 20, color = "white", boxcolor = "black",
                 location = "+80+220", font = "Impact") %>%
  image_annotate("Online Lectures", size = 20, color = "white", boxcolor = "black",
                 location = "+360+230", font = "Impact")
image_2 <- image_read("image2.png") %>%
  image_scale("x300") %>% image_border("#000000", "4x4") %>%
  image_annotate("Completely\nreasonable\ndeadlines", size = 20, color = "white",
                 boxcolor = "black", location = "+70+150", font = "Impact")
captions <- image_blank(width = 525, height= 40, color = "#000000") %>%
  image_annotate("What having bad time management is like:", size = 25,
                 color = "white", location = "+46+3", font = "Impact")
image_vector <- c(captions, image_1, image_2)
meme <- image_append(image_vector, stack = TRUE)
image_write(meme, "rip_meme.png")
```
## Meme Originality
My meme was derived from the ["drowning man meme format"](https://memegenerator.net/Drowning-Man-Sitting-2022/caption), along with the following **original features:**
- A custom border
- A caption at the top
- Custom captions
- My amazing creativity and artistic touch
