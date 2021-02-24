# AutoQuote
A VS Code snippet key binding
to convert `array of number` to `array of string` quickly

[1, 2, 3] => ['1', '2', '3']

or format a object:
{
    a: 1,
    b: 2,
    c: 3,
}
=>
{
    'a': '1',
    'b': '2',
    'c': '3',
}

## Demo

![demo](https://raw.githubusercontent.com/huskylin/AutoQuote/master/AutoQuoteDemo.gif)

## Usage
1. open keybindings.json
    shortcut: `Ctrl+K` + `Ctrl+S`
2. click this ![icon](https://imgur.com/eciQSyJ)
3. Copy and paste to your snippet setting file
    ``` JSON
    [
        {
            "key": "alt+b",
            "command": "editor.action.insertSnippet",
            "args": {
                "snippet": "${TM_SELECTED_TEXT/([^,\\[\\]\\s:{}]+)(,)?/'$1'${2:+,}/g}"
            }
        }
    ]
    ```

## 使用方法
開啟快捷鍵設定檔：keybindings.json

開啟步驟如下：

1. 將滑鼠挪到左下角的齒輪後，點擊。
    找到鍵盤快速鍵後，點擊。
    會開啟類似 GUI 功能的介面。
    ( 或是用快捷鍵 先按 `Ctrl+K` 然後按 `Ctrl+S` )
2. 將滑鼠挪到右上角，找尋此圖示後，點擊。
    ![icon](https://imgur.com/eciQSyJ)
3. 貼上
    ``` JSON
    [
        {
            "key": "alt+b",
            "command": "editor.action.insertSnippet",
            "args": {
                "snippet": "${TM_SELECTED_TEXT/([^,\\[\\]\\s:{}]+)(,)?/'$1'${2:+,}/g}"
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

