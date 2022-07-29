# PET Game Patches for Business Keyboards

### What is this?

As the keyboard hardware differs between different models of Commodore PET, sofware written for the original "Graphics keyboard" might not work properly - or at all - with "Business keyboard"-PET. This repository contains binary patches so you can modify your existing files so that they will then work with business keyboards.

### How does it work?

To apply a patch, follow the following simple steps:

1. First check that the game file you have is suitable for the patch by verifying that you have the same checksum as what's listed in the table below: 
```
$ md5sum afo\ with\ sound.prg 
22e85348d279c60d7a83deefcbf04b85afo with sound.prg
```
2. Then apply the patch with bspatch to generate a new file:
```
$ bspatch afo\ with\ sound.prg afo.prg afo\ with\ sound.bsdiff
```

### List of games

| Game             | MD5 checksum                        | Patch file            | What does it do? |
| ---------------- | ----------------------------------- | --------------------- | ---------------- |
| AFO (with sound) | 22e85348d279c60d7a83deefcbf04b85afo | afo with sound.bsdiff | Fixes controls   |