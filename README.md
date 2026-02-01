# 2026 Gedit Documents Panel Bug Fixing Challenge

## Bug description

The Documents Panel in Gedit does not support touchscreen well on Wayland. Each tab in the Documents Panel can be dragged via mouse. However, they cannot be dragged via touchscreen. Touch screen works well on other parts of Gedit. On Xorg (a.k.a. X11) this bug does not happen.

Gedit can be installed via `sudo apt install gedit` on Debian 13. The Documents Panel can be seen after enabling the side panel.

This video shows the buggy behavior and the expected behavior (after applying my workaround): <https://youtu.be/Ky-T02QUYSw>

## Repo setup

The relevant source code is provided under the `src` directory:
* [gedit](https://packages.debian.org/trixie/gedit) 48.1-4
* [glib2.0](https://packages.debian.org/trixie/libglib2.0-0t64) 2.84.4-3~deb13u2
* [gtk+3.0](https://packages.debian.org/trixie/libgtk-3-0t64) 3.24.49-3

## Goal

The goal is to fix/workaround this bug. At least the Documents Panel should respond to touchscreen drag events.

The workaround should not be too complicated. For example if it is more than 100 lines of code it is definitely too complicated.

## Workaround

I have already found a workaround. (Even though the workaround is not perfect.)

I am not publishing it at this point. To prove I have the workaround, here are the hash values:

```
md5: a315ab79e37dc246492f90fb02d26438
sha1: 8ee0de908a245fda7c8af421cbbf41498341a399
sha256: 6db96038355d1f67a77588827883c9277a146f863e866eb02e04817140ae0938
sha512: 62560e6e765b25f709d0635732d2d2ac3dea432064ecb2d55d057ea0c835df198f5eb61393b586a78aac55b8088d0696307d07d864ba7ac7c7f7150dddcf9491
```

## Timeline

This challenge is published around 20 Jan 2026 00:00 (UTC). I am planning to publish my workaround around 1 Feb 2026 00:00 (UTC). This time is subject to change.

## Solution

The solution is published under `solution/` and `solution.tgz`.

Video: <https://youtu.be/9QSQzxLsh9w>

### Bug reports

* <https://gitlab.gnome.org/GNOME/gtk/-/issues/8008>
	* <https://gitlab.gnome.org/GNOME/gtk/-/merge_requests/9418>

