# My DWM build

This is my dwm build patched from scratched including the systray patch. Other patches including in this build are:

- uselessgaps
- autostart (some manual patching needed)
- fixborders
- movestack
- statusallmon
- warp
- attachaside
- alwasyceter
- restartsig
- pertag
- scratchpads
- zoomswap
- focusonnetactive
- statuspadding


Additionally, libxft-bgra has been installed from the AUR so color icons are shown in the status bar. The following lines have to be commented out (or deleted from `drw.c`) for this to work:

```c
FcBool iscol;
	if(FcPatternGetBool(xfont->pattern, FC_COLOR, 0, &iscol) == FcResultMatch && iscol) {
		XftFontClose(drw->dpy, xfont);
		return NULL;
	}
```
