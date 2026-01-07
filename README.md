# Rex.Oh-MY-Posh
setup guide to a customized Terminal UI on Powershell using using **Oh My Posh**, Nerd Fonts, and a custom JSON theme.

## 🧰 Requirements

- **PowerShell 7+**
- **Oh My Posh** (installed locally)
- **Nerd Font** (required for icons)
  - Recommended:
    - `FiraCode Nerd Font Mono`
 NOTE=> Download Nerd Fonts from Web

If Oh My Posh is not installed yet:
```winget install JanDeDobbeleer.OhMyPosh```

Verify:
```oh-my-posh --version```

🔧 PowerShell Profile Setup (Manual Method)
Open your PowerShell profile
```notepad $PROFILE```

If it doesn’t exist:
```New-Item -ItemType File -Path $PROFILE -Force```

In settings.json of terminal, add/edit this in list array in profiles object  :
``` {
                "colorScheme": "Campbell",
                "font": 
                {
                    "face": "FiraCode Nerd Font Mono"
                },
                "guid": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
                "hidden": false,
                "name": "PowerShell",
                "opacity": 99,
                "source": "Windows.Terminal.PowershellCore",
                "useAcrylic": true
            }
```

Locate ohmyposh's path on your system & also add my theme/ recreate a different theme to enhance the feel of Terminal UI (e.g.):
```& "~\Local\Programs\oh-my-posh\bin\oh-my-posh.exe" init pwsh --config "~\Local\Programs\oh-my-posh\themes\rexTHeme.omp.json" | Invoke-Expression```

