# AutoQuote
A VS Code snippet key binding
to convert `array of number` to `array of string` quickly

[1, 2, 3] => ['1', '2', '3']

## Demo

![demo](https://raw.githubusercontent.com/huskylin/AutoQuote/master/AutoQuoteDemo.gif)

## Usage
Copy and paste to your snippet setting file
``` JSON
[
    {
        "key": "alt+b",
        "command": "editor.action.insertSnippet",
        "args": {
            "snippet": "${TM_SELECTED_TEXT/([^,\\[\\]\\s]+)(,)?/'$1'${2:+,}/g}"
        }
    }
]
```

## More info about snippets
[VS Code Official Docs](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_assign-keybindings-to-snippets)
> ## Assign keybindings to snippets
> You can create custom [keybindings](https://code.visualstudio.com/docs/getstarted/keybindings) to insert specific snippets. Open `keybindings.json` (Preferences: Open Keyboard Shortcuts File), which defines all your keybindings, and add a keybinding passing `"snippet"` as an extra argument:
> ``` JSON
> {
>   "key": "cmd+k 1",
>   "command": "editor.action.insertSnippet",
>   "when": "editorTextFocus",
>   "args": {
>     "snippet": "console.log($1)$0"
>   }
> }
> ```

