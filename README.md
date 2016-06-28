# chinese-holidays

### Install

    npm install chinese-holidays


### Usage


```javascript
var ChineseHolidays = require('chinese-holidays');

元旦 = new Date(2016, 0, 1)
// 是否休假(含正常的周六、周日)
ChineseHolidays.isHoliday(元旦)     # true
// 是否是工作日(含节假日的调休)
ChineseHolidays.isWorkingday(元旦) # fase


// 列出已知的特殊节假日
ChineseHolidays.all().forEach(function(holiday){
  console.log(holiday.name)
  console.log(holiday.days().map(function(date) { return moment(date).format('YYYY-MM-DD') }))
})
// 元旦
// ["2016-01-01", "2016-01-02", "2016-01-03"]
// ...
```