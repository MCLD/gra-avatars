# Great Reading Adventure Avatars

This repository contains the default avatar files for [The Great Reading Adventure](https://github.com/MCLD/greatreadingadventure/) ([mirror](https://codeberg.org/MCLD/greatreadingadventure)), a robust, open source software designed to manage library reading programs online. The GRA is free to use, modify, and share. Check out [www.greatreadingadventure.com](https://www.greatreadingadventure.com/) for an overview of its functionality and capabilities.

The majority of the avatar artwork originated in [Glitch the Game](https://web.archive.org/web/20240820054744/https://www.glitchthegame.com/public-domain-game-art/) ([GitHub](https://github.com/orgs/tinyspeck/repositories?q=glitch)) and was used via their [Creative Commons CC0 1.0 Universal License](http://creativecommons.org/publicdomain/zero/1.0/legalcode).

Additional items are added (usually to support the [Maricopa County Reads](https://maricopacountyreads.org/) summer reading program managed by the [Maricopa County Library District](https://mcldaz.org/) who manages this package and The Great Reading Adventure software.)

## Usage

When using a release of The Great Reading Adventure, importing the default avatars in Mission Control will import the avatars from this collection. If you are using a release which does not include the default avatar file you can [download it here](https://github.com/MCLD/gra-avatars/releases/latest) and import it.

**Be aware that as of version 5 of this package you must be running GRA version 4.7.0 or later as the import/export format for avatars has changed. If you are running a prior version of the GRA you will need [release v4.2.2](https://github.com/MCLD/gra-avatars/releases#release-v4.2.2) of the avatar package.**

## Using custom avatars

The default avatar package includes over 5,500 elements. If the desire is to use custom avatars in place of the default avatars, the software can accept and layer 300x500 pixel `.PNG` files. Once you install the GRA you can manage avatars in Mission Control.

The default GRA stylesheet includes cropping based on the way the default avatars display, for example: on mobile devices the only part of the avatar which shows is the head and head accessories. If you are using custom images and want to override the default cropping, add the following to `content/site1/styles/site.css` file in the shared directory:

```css
.avatar-container-dashboard {
  height: 400px;
}

@media only screen and (min-width: 768px) {
  .avatar-container-dashboard {
    height: 250px;
  }
}

@media only screen and (min-width: 992px) {
  .avatar-container-dashboard {
    height: 350px;
  }
}

@media only screen and (min-width: 1200px) {
  .avatar-container-dashboard {
    height: 425px;
  }
}
```

## License

Much like the original art from Glitch the Game, art in this repository is licensed under the [Creative Commons CC0 1.0 Universal License](https://github.com/MCLD/gra-avatars/blob/main/LICENSE).

