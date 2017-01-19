# utils
GoSublime config
{
    "env": {
        "GOPATH": "$HOME/go",
        "PATH": "$PATH:$GOPATH/bin",
    },

    "comp_lint_enabled": true,
    "autocomplete_suggest_imports": true,

    "fmt_cmd": [
        "goimports"
    ],

    "on_save": [
        {"cmd": "gs_comp_lint"},
    ],

    "comp_lint_commands": [
        {"cmd": ["goimports -w $_fn"] , "shell": true},
        {"cmd": ["golint $_fn"], "shell": true},
        {"cmd": ["go", "vet"]},
    ],
}