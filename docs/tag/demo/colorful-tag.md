# 彩色标签

- order: 1

在非 `closeable` 和 `selectable` 类型下，可以通过增加 `color` 属性来为 tag 设置自定义颜色。


:::lang=en-us
# Colorful Tag

- order: 1

you can set custom color for `Tag` by adding `color` properity when it's neither  `closable` nor `selectable` mode

:::

---

```jsx
import { Tag, Icon } from '@alifd/next';

const {Group: TagGroup} = Tag;

const presetColors = ['success', 'error', 'warning', 'info', 'help'];
const customColos = ['#f50', '#2db7f5', '#87d068', '#108ee9'];

ReactDOM.render(<div className="tag-list">
    <h4>presets</h4>
    <TagGroup>
    {
        presetColors.map(color=><Tag key={`normal-${color}`} type="normal" color={color}>{color}</Tag>)
    }
    </TagGroup>

    <TagGroup>
    {
        presetColors.map(color=><Tag key={`primary-${color}`} type="primary" color={color}>{color}</Tag>)
    }
    </TagGroup>

    <h4>custom colors</h4>
    <TagGroup>
    {
        customColos.map(color=><Tag key={`normal-${color}`} type="normal" color={color} size="small">{color}</Tag>)
    }
    </TagGroup>

    <TagGroup>
    {
        customColos.map(color=><Tag key={`primary-${color}`} type="primary" color={color} size="large">{color}</Tag>)
    }
    </TagGroup>
</div>,
mountNode);
```
