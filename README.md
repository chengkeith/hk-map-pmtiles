# hk-pmtiles-generation
Github Action to generate Hong Kong PMTiles every few days automatically and publish to Github Pages

### Usage
Fork this repo, setup GitHub pages and make sure you have Actions enabled :)
You might also want to use https://github.com/marketplace/actions/keepalive-workflow to keep your fork alive, preventing the scheduled actions from being disabled

### Attribution

The tilesets that power the generated PMTiles are Produced Works of the OpenStreetMap dataset under the Open Database License. Web maps and native apps that use this Produced Work must visibly attribute © OpenStreetMap - for example, in the corner of the map display.

### Disable generation of a specific type
#### For manual workflow runs:
When manually triggering the workflow, uncheck any of these options:
- Build vector tiles
- Build labels tiles
- Build raster light tiles
- Build raster dark tiles

#### For scheduled runs:
Edit the environment variables in `.github/workflows/generate-maptiles.yml`:
```yaml
env:
  CRON_BUILD_VECTOR: true
  CRON_BUILD_LABELS: true
  CRON_BUILD_RASTER_LIGHT: true
  CRON_BUILD_RASTER_DARK: true
```

### Styles

The default styles are adopted from Protomaps with slight modifications so it looks better in lower resolutions.

You can modify the styles yourself on the two files at the repo root