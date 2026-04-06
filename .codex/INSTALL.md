# Beagle for Codex

Install Beagle into Codex's skill path with the repo helper script.

```bash
./install-codex-skills.sh
```

By default this creates or updates symlinks under `~/.agents/skills/` for each maintained Beagle plugin.

To use a different destination:

```bash
BEAGLE_SKILLS_DEST=/some/other/skills ./install-codex-skills.sh
```

Manual single-plugin example:

```bash
ln -sfn "/path/to/beagle/plugins/beagle-core/skills" "$HOME/.agents/skills/beagle-core"
```

Windows junction example:

```bat
REM Run from the Beagle checkout, or replace the source path below.
mklink /J "%USERPROFILE%\.agents\skills\beagle-core" "C:\path\to\beagle\plugins\beagle-core\skills"
```

Update note: `git pull` in the Beagle checkout updates installed skills immediately because the links point into the repo.
