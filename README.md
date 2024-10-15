# Useful-VSCode
Add this in keybindings.json for easier commenting.

Shift+* to add code into comment blocks /* selected text */ or in html <!-- selected text -->

You can click it again to remove commented blocks

Open with CTRL+SHIFT+P, search for "Open Keyboard Shortcuts (JSON)"

    // comment out code for typescript, javascript, css, json, jsonc
    {
        "key": "Shift+oem_2",
        "command": "editor.action.blockComment",
        "when": "editorTextFocus && editorHasSelection && (editorLangId == 'typescript' || editorLangId == 'javascript' || editorLangId == 'css' ||  editorLangId == 'json' || editorLangId == 'jsonc')",
        "args": {
            "snippet": "/*${TM_SELECTED_TEXT}*/"
        }
    },

    // quick add comment block for typescript, javascript, css, json, jsonc
    {
        "key": "Ctrl+Shift+oem_2",
        "command": "editor.action.blockComment",
        "when": "!editorHasSelection && (editorLangId == 'typescript' || editorLangId == 'javascript' || editorLangId == 'css' ||  editorLangId == 'json' || editorLangId == 'jsonc')",
        "args": {
            "snippet": "/* $0 */"
        }
    },

    // comment out code for html
    {
        "key": "Shift+oem_2",
        "command": "editor.action.blockComment",
        "when": "editorTextFocus && editorHasSelection && (editorLangId == 'html')",
        "args": {
            "snippet": "<!--${TM_SELECTED_TEXT}-->"
        }
    },

    // quick add comment block for html
    {
        "key": "Ctrl+Shift+oem_2",
        "command": "editor.action.blockComment",
        "when": "!editorHasSelection && (editorLangId == 'html')",
        "args": {
            "snippet": "<!-- $0 -->"
        }
    },
