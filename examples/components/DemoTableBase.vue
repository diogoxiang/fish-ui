<template>
  <fish-table :columns="columns" :data="data"></fish-table>
</template>
<script>
  export default {
    name: 'demo-table-base',
    data () {
      return {
        columns: [{title: 'Name', key: 'name'},
          {title: 'age', key: 'age'},
          {title: 'Address', key: 'address'},
          {title: 'Operate',
            key: 'operate',
            render: (h, record, column) => h('a', '编辑')}],
        data: [
          {name: 'yanbin.hu', age: 32, address: 'haidi part 1, xihu, Hangzhou'},
          {name: 'yanzu.wu', age: 35, address: 'haidi part 5, xihu, Hangzhou'},
          {name: 'yanzu.wu', age: 35, address: 'haidi part 5, xihu, Hangzhou'},
          {name: 'yanzu.wu', age: 35, address: 'haidi part 5, xihu, Hangzhou'}
        ]
      }
    }
  }
</script>