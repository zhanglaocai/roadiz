<template>
    <drawer-item
        :item="item"
        :index="index"
        :drawer-name="drawerName"
        :is-item-explorer="isItemExplorer"
        :parent-name="item.parent ? item.parent.title : ''"
        :sub-parent-name="item.subparent ? item.subparent.title : ''"
        :name="item.title ? item.title : item.nodeName"
        :is-pusblished-class="item.isPublished ? '' : 'not-published'"
        :edit-item="item.nodesEditPage"
        :add-item="addItem"
        :remove-item="removeItem">
    </drawer-item>
</template>
<script>
    import DrawerItem from './DrawerItem.vue'

    export default {
        props: [
            'item',
            'trans',
            'isItemExplorer',
            'drawerName',
            'index',
            'removeItem',
            'addItem'
        ],
        components: {
            DrawerItem
        }
    }
</script>
