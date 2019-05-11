# el-tree-select

基于element-ui扩展的一个TreeSelect组件

使用方式：
<el-tree-select :data="treeData" v-model="value1" node-key="id" size="mini" />
属性：
props: {
    value: {
        type: [String, Number, Array]
    },
    multiple: {
        type: Boolean,
        default: false
    },
    disabled: {
        type: Boolean,
        default: false
    },
    size: {
        type: String,
        default: 'default'
    },
    clearable: {
        type: Boolean,
        default: false
    },
    collapseTags: {
        type: Boolean,
        default: true
    },
    name: {
        type: String
    },
    placeholder: {
        type: String
    },
    data: {
        type: Array
    },
    emptyText: {
        type: String,
        default: '暂无数据'
    },
    nodeKey: {
        type: String,
        required: true
    },
    props: {
        type: Object,
        default: function () {
            return {
                label: 'label',
                children: 'children',
                disabled: 'disabled'
            }
        }
    },
    defaultExpandAll: {
        type: Boolean,
        default: true
    },
    expandOnClickNode: {
        type: Boolean,
        default: false
    },
    checkOnClickNode: {
        type: Boolean,
        default: true
    },
    checkStrictly: {
        type: Boolean,
        default: true
    },
    accordion: {
        type: Boolean,
        default: false
    }
}
事件：
change
remove-tag
