# prettymaps

This is a fork of the [`prettymaps`](https://github.com/marceloprates/prettymaps) library, providing support for [rectangular maps](https://github.com/marceloprates/prettymaps/pull/105), as well as a `prettymaps` map generation CLI.


## Installation

This fork hasn't been published to PyPI, meaning you should `pip` install it from Github directly:

```bash
% pip install "git+https://github.com/brouberol/prettymaps.git"
```

This will install the library and will put a `prettymaps` executable script in your `PATH`.

## CLI usage

```
Usage: prettymaps [OPTIONS]

  Artistic map generation CLI, based on the prettymaps library

  Examples:

      # generate a map for the argument location
      $ prettymaps --location <address>

      # generate a circular map
      $ prettymaps --location <address> --circle

      # generate a circular map with the theme based off the matplotlib colormap Set3
      $ prettymaps --location <address> --circle --theme Set3

      # Generate a map of the area 2000m around the provided location
      $ prettymaps --location <address> --radius 2000

Options:
  --location TEXT                 The address to geocode and use as the
                                  central point around which to get the
                                  geometries  [required]
  --radius INTEGER                Radius, in meters, around the provided
                                  location  [default: 1000]
  --circle                        If true, the map will be represented as a
                                  circle, and as a square if not.
  --format [square|A3|A2|A1|A0]   The output dimenions of the map  [default:
                                  A3]
  --theme [old-school|default|tartan|royal-stewart|royal-stewart2|royal-stewart3|magma|inferno|plasma|viridis|cividis|twilight|twilight_shifted|turbo|Blues|BrBG|BuGn|BuPu|CMRmap|GnBu|Greens|Greys|OrRd|Oranges|PRGn|PiYG|PuBu|PuBuGn|PuOr|PuRd|Purples|RdBu|RdGy|RdPu|RdYlBu|RdYlGn|Reds|Spectral|Wistia|YlGn|YlGnBu|YlOrBr|YlOrRd|afmhot|autumn|binary|bone|brg|bwr|cool|coolwarm|copper|cubehelix|flag|gist_earth|gist_gray|gist_heat|gist_ncar|gist_rainbow|gist_stern|gist_yarg|gnuplot|gnuplot2|gray|hot|hsv|jet|nipy_spectral|ocean|pink|prism|rainbow|seismic|spring|summer|terrain|winter|Accent|Dark2|Paired|Pastel1|Pastel2|Set1|Set2|Set3|tab10|tab20|tab20b|tab20c|magma_r|inferno_r|plasma_r|viridis_r|cividis_r|twilight_r|twilight_shifted_r|turbo_r|Blues_r|BrBG_r|BuGn_r|BuPu_r|CMRmap_r|GnBu_r|Greens_r|Greys_r|OrRd_r|Oranges_r|PRGn_r|PiYG_r|PuBu_r|PuBuGn_r|PuOr_r|PuRd_r|Purples_r|RdBu_r|RdGy_r|RdPu_r|RdYlBu_r|RdYlGn_r|Reds_r|Spectral_r|Wistia_r|YlGn_r|YlGnBu_r|YlOrBr_r|YlOrRd_r|afmhot_r|autumn_r|binary_r|bone_r|brg_r|bwr_r|cool_r|coolwarm_r|copper_r|cubehelix_r|flag_r|gist_earth_r|gist_gray_r|gist_heat_r|gist_ncar_r|gist_rainbow_r|gist_stern_r|gist_yarg_r|gnuplot_r|gnuplot2_r|gray_r|hot_r|hsv_r|jet_r|nipy_spectral_r|ocean_r|pink_r|prism_r|rainbow_r|seismic_r|spring_r|summer_r|terrain_r|winter_r|Accent_r|Dark2_r|Paired_r|Pastel1_r|Pastel2_r|Set1_r|Set2_r|Set3_r|tab10_r|tab20_r|tab20b_r|tab20c_r]
                                  The color theme to use, chosen among the
                                  hardcoded list of themes or matplotlib
                                  colormaps (see https://matplotlib.org/stable
                                  /gallery/color/colormap_reference.html for
                                  the complete list)  [default: default]
  --vertical                      Orient the generated map vertically if true
  --river-overflow                Let rivers overflow from the map if true
  --background-color TEXT         The HTML background color  [default:
                                  #ffffff]
  --margins-mm INTEGER            The margin size, in mm, to place around the
                                  map. Useful for print jobs..  [default: 0]
  --scaling-factor INTEGER        The scaling factor applied on the final
                                  generated image.  [default: 1]
  --padding INTEGER               The padding to be applied around the map.
                                  [default: 100]
  --cmd-as-title                  If true, set the map title as the prettymaps
                                  CLI command used to generate it
  -o, --output-dir TEXT           The directory to store the map under
  --dpi INTEGER                   Number of pixels per inch  [default: 100]
  --bw                            Generate a black & white map
  --help                          Show this message and exit.
```

You can refer to the [`examples/`](https://github.com/brouberol/prettymaps/tree/main/examples) directory, as each map will be titled after the command that was executed to generate it.

## Original project README

Follow this [link](https://github.com/marceloprates/prettymaps/blob/main/README.md).