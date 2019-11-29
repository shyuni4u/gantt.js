# gantt.js
Gantt chart used vanillajs

<hr/>

## 1. Just open simple.html file

```HTML
<div id="gantt_here" style="width:100%;height:650px;"></div>
...
<script>
let s_date_1	= $('[name="sDate_1"]').val();
let s_date_2	= $('[name="sDate_2"]').val();
let n_count   = remove_comma_Number($('[name="nCount"]').val());

let from	= new Date(s_date_1);
let to		= new Date(s_date_2);

gantt.tasks = generateData(n_count, from, to);

gantt.config.start_date = from;
gantt.config.end_date = to;

gantt.config.min_column_width = 35;
gantt.config.min_column_height = 25;
gantt.config.use_add = false;
gantt.config.left_type = [
  {title: 'PROJECT', width: '170', align: 'left', content: 'cfg_name'},
  {title: 'PROCESS', width: '180', align: 'left', content: 'pc_name'},
  {title: 'Start Date', width: '90', align: 'left', content: 'start'},
  {title: 'End Date', width: '90', align: 'left', content: 'end'},
  {title: 'Man-Hour', width: '60', align: 'left', content: 'capa'}
];

gantt.config.fn_after_reset = make_bottom;
gantt.config.fn_scroll_horizon = move_bottom;

gantt.init_gantt('gantt_here');
</script>
```

## 2. example.html file is used echart.js
