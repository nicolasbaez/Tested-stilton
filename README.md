# Tested-stilton
You're never prepared for the storm.

![buh](https://github.com/nicolasbaez/Tested-stilton/blob/main/xp070.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
k = 0.1;
draw = (_) => {
  h = w / 2;
  f = random(map((sin(PI * k) / PI) * k, -1, 1, 0, h));
  background(0, f, f);
  for (i = 0; i < 99; i++) {
    stroke(h);
    x = random(w);
    y = random(w);
    d = random(w / 9);
    line(x, y, x + d, y + d);
  }
  k += 0.005;
  if (frameCount == 1)
    saveGif("xp070.gif", 1500, { delay: 0, units: "frames" });
};
