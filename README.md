# area-data
中国行政区域数据(含港澳台),包含深圳10区域

## Installation
Install the pkg with npm:

```
npm install union-area-data --save
```

or yarn

```
yarn add union-area-data
```

or bower

```
bower install union-area-data
```

## 获取数据
```
// v5之前的版本
import AreaData from 'union-area-data';

// v5及之后的版本
import { pca, pcaa } from 'union-area-data';
// 可以根据需要按需引入：
import PCA from 'union-area-data/pca'; 
import PCAA from 'union-area-data/pcaa'; 

pca['86'] // 等同于 AreaData['86']
// 所有省份：{'110000': '北京市', '120000': '天津市', '130000': '河北省', ...}

pcaa['130000'] // 等同于 AreaData['130000']
// 对应省份的所有城市：{'130100': '石家庄市', '130200': '唐山市', '130300': '秦皇岛市', ...}

pcaa['130200'] // 等同于 AreaData['130200']
// 对应市的所有县区：{'130201': '市辖区', '130202': '路南区', '130203': '路北区', ...}

### v1
AreaData['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}
```

> 官方数据(截止到2016.07.31): [城乡区域划分](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)

**数据来源：** 最新省市区数据来自 [area-puppeteer](https://github.com/dwqs/area-puppeteer/).

## LICENSE

MIT

