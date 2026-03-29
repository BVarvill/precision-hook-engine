# Precision Hook Engine

Outreach hook generator for conference lead engagement. Reads researcher notes on each lead, selects the most relevant conference subtheme, matches against a library of previous productions, and generates a tailored hook paragraph and full outreach email.

## What It Does

1. **Reads** your hand-written researcher notes from the Hub spreadsheet
2. **Selects** the best-fit conference subtheme from a structured taxonomy
3. **Matches** up to 3 relevant past productions from the film library based on institution type and topic
4. **Generates** a precise, fact-grounded hook paragraph — no hallucinated details, only what's in your notes
5. **Assembles** the full outreach email from a fixed template with the generated hook slotted in
6. **Syncs** the Hook Generator tab with the master leads list, removing any deleted leads

## Usage

```bash
python3 generate_apa_hooks.py                    # All leads with notes ready
python3 generate_apa_hooks.py --row 5            # Single lead by hub row
python3 generate_apa_hooks.py --dry-run          # Preview without generating
python3 generate_apa_hooks.py --sync             # Remove orphaned leads from Hook Generator
python3 generate_apa_hooks.py --auto-research    # Auto-fill research notes via Serper API
```

## Requirements

- Python 3.8+
- `openpyxl` — `pip install openpyxl`
- LLM CLI tool for hook generation
- Hub spreadsheet (`APA_2026_Combined_Hub.xlsx`) with tabs: Ben Leads Ready, Hook Generator, Film Library
