# Method `Au.Types.RECT.Inflate`

Makes this rectangle bigger or smaller: `left-=dx; right+=dx; top-=dy; bottom+=dy;` Use negative *dx*/*dy* to make the rectangle smaller. Note: too big negative *dx*/*dy* can make it invalid (`right < left` or `bottom < top`).

```
public void Inflate(int dx, int dy)
```

##### Parameters

- *dx*  (`int`)
- *dy*  (`int`)