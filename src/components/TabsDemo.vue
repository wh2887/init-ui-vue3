<template>
  <h1>Tabs 组件示例</h1>
  <p style="margin: 10px 0;color: #636366;font-size: 14px;">
    分隔内容上有关联但属于不同类别的数据集合。
  </p>
  <Demo :component="Tabs1Demo" description="默认选中 '导航1'。 "/>
  <APIDemo :describe="describe"/>
</template>

<script lang="ts">
import Tabs1Demo from './demo-code/Tabs1Demo.vue';
import Demo from './Demo.vue';
import APIDemo from './APIDemo.vue';

export default {
  components: {APIDemo, Demo, Tabs1Demo},
  setup() {
    const describe = [
      {attribute: 'selected', explain: '当前激活 tab 面板的 title', type: 'string', defaultValue: '---'},
      {attribute: 'title', explain: 'Tab 组件的参数，用于父组件定位', type: 'string', defaultValue: '---'},
    ];
    return {Tabs1Demo,describe};
  }
};
</script>
