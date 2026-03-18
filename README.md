# Retro Monitor Repair Wiki

A comprehensive technical documentation website for repairing vintage CRT monitors, built with MkDocs and Material for MkDocs.

## Features

- Complete repair guides for Commodore Amiga 1080 monitor
- Step-by-step troubleshooting flowcharts
- Safety warnings and precautions
- High-quality technical documentation
- Responsive design with dark/light mode
- Full-text search
- Automatic table of contents

## Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/NoodleStormno/retromonitor.git
   cd retromonitor
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Preview the site locally:
   ```bash
   mkdocs serve
   ```

4. Build the site:
   ```bash
   mkdocs build
   ```

## Project Structure

```
retromonitor/
├── docs/
│   ├── index.md                    # Homepage
│   ├── images/                     # All images
│   └── monitors/
│       └── commodore/
│           └── amiga1080/          # Commodore Amiga 1080 repair guides
├── mkdocs.yml                      # MkDocs configuration
├── requirements.txt                # Python dependencies
└── README.md                       # This file
```

## Deployment

This site is configured for GitHub Pages deployment. The `site/` directory should not be committed to the repository.

To deploy manually:
```bash
mkdocs gh-deploy
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add or update documentation
4. Submit a pull request

## License

All content is provided for educational purposes only. Repairing CRT monitors involves high voltage and should only be attempted by qualified technicians.

## Safety Notice

⚠️ **CRT MONITORS CONTAIN LETHAL VOLTAGES!**

- Always discharge the picture tube anode before handling
- Use proper high-voltage probes and insulated tools
- Work in a well-ventilated area
- Never work alone on high-voltage equipment
- If unsure, consult a qualified technician