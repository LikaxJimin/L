# L
What colour is the word?
from PIL import Image, ImageDraw

images = []
out = Image.new("RGB", (1000, 1000), (255, 255, 255))
width = 300
height = 300
center = width // 2
color_1 = (0, 0, 0)
color_2 = random(r,g,b)
color_3 = random(r,g,b)

for i in range(100):
    im = Image.new('RGB', (width, width), color_1)
    draw = ImageDraw.Draw(im), 
    draw.rectangle((10, 10, 600, 600) fill=color_2)
    images.append(im)
    
 for i in range(100):
    im = Image.new('RGB', (width, width), color_1)
    draw = ImageDraw.Draw(im), 
    draw.rectangle((390, 390, 600, 600) fill=color_3)
    images.append(im)
    

    # get a font
    fnt = ImageFont.truetype("Pillow/Tests/fonts/FreeMono.ttf", 60)
    # get a drawing context
    d = ImageDraw.Draw(out)

    # draw multiline text
    d.multiline_text((100,800), "White\Black\Grey\Yellow\Red\Blue\Green\Brown\Pink\Orange\Purple", font=fnt, fill=(0, 0, 0))    
  

images[0].save('data/dst/pillow_imagedraw.gif',
               save_all=True, append_images=images[1:], optimize=False, duration=40, loop=0)
