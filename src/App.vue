<template>
    <div>
      <p>(You can double click on an item to turn it into a folder.)</p>
        <ul>
          <item
          class="item"
          :model="treeData"
          >
          </item>
        </ul>
    </div>
</template>

<script>
import item from './components/Item'
var data = {
    name: 'My Tree',
    children: [
        { name: 'hello' },
        { name: 'wat' },
        {
            name: 'child folder',
            children: [
                {
                    name: 'child folder',
                    children: [
                        { name: 'hello' },
                        { name: 'wat' }
                    ]
                },
                { name: 'hello' },
                { name: 'wat' },
                {
                    name: 'child folder',
                    children: [
                        { name: 'hello' },
                        { name: 'wat' }
                    ]
                }
            ]
        }
    ]
}
export default {
    name: 'App',
    data () {
        return {
            treeData: data
        }
    },
    components: {
        item
    }
}
</script>

<style scoped>
body {
  font-family: Menlo, Consolas, monospace;
  color: #444;
}
.item {
  cursor: pointer;
}
.bold {
  font-weight: bold;
}
ul {
  padding-left: 1em;
  line-height: 1.5em;
  list-style-type: dot;
}
</style>
