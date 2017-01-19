# utils

Context.sublime-menu need to put into Package dir

## Sublime config
```json
{
    "font_size": 11,
    "ignored_packages":
    [
        "Vintage"
    ],
    "rulers":
    [
        120
    ],
    "scroll_speed": 2.0,
    "show_encoding": true,
    "translate_tabs_to_spaces": true
}

```

## GoSublime config
```json
{
    "env": {
        "GOPATH": "$HOME/go",
        "PATH": "$PATH:$GOPATH/bin",
    },

    "fmt_tab_width": 4,

    "comp_lint_enabled": true,
    "autocomplete_suggest_imports": true,

    "fmt_cmd": [
        "goimports"
    ],

    "comp_lint_commands": [
        {"cmd": ["goimports -w $_fn"] , "shell": true},
        {"cmd": ["golint $_fn"], "shell": true},
        {"cmd": ["go", "vet"]},
    ],

    "autocomplete_tests": true,
    "autocomplete_builtins": true,
    "autocomplete_closures": true,
    "autocomplete_suggest_imports": true,

    "on_save": [
        {"cmd": "gs_comp_lint"},
    ],
}
```
