# 3sqrt7-context-menu
 一款适用于 HTML 的右键菜单组件。

## 示例

### HTML

```html
<link rel="stylesheet" type="text/css" href="contextMenu.css">
<script type="text/javascript" src="contextMenu.js"></script>
```

### JS

```js
window.addEventListener("contextmenu", (evt) => {
    evt.preventDefault();
    new ContextMenu([
        {
            label: "#1",
            click() {
                // do something...
            }
        }, {
            label: "#2",
            disabled: true
        }, {
            type: "separator"
        }, {
            label: "#3",
            submenu: []
        }, {
            label: "#4",
            submenu: [
                {
                    label: "#5",
                    click() {
                        // do something...
                    }
                }
            ]
        }
    ]).popup([evt.clientX, evt.clientY]);
});
```

