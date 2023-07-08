For the laptop's retina display, the default setting looks very good. 

```
defaults -currentHost delete -g AppleFontSmoothing 
```


For external displays with less than 4K resolution, this looks better:
```
defaults -currentHost write -g AppleFontSmoothing -int 0
```

After changing the setting, you must log-out so works.


Also, when using an external display, non-antialiased fonts tend to look better (at least for programming). Tamzen and Tamsyn fonts are nice.
