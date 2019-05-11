<template>
    <el-row>
        <el-form size="mini">
            <el-col :span="8">
                <el-form-item label="单选：">
                    <el-tree-select :data="treeData" v-model="value1" node-key="id" size="mini" />
                </el-form-item>
            </el-col>
            <el-col :span="8">
                <el-form-item label="多选:">
                    <el-tree-select :data="treeData" v-model="value2" node-key="id" size="mini" :multiple="true" />
                </el-form-item>
            </el-col>
            <el-col :span="8">
                <el-form-item label="禁用:">
                    <el-tree-select :data="treeData" v-model="value3" node-key="id" size="mini" :multiple="true" :disabled="true" />
                </el-form-item>
            </el-col>
        </el-form>
    </el-row>
</template>

<script>
import ElTreeSelect from './ElTreeSelect/index.vue'

export default {
    name: 'MainPage',
    components: {
        'el-tree-select': ElTreeSelect
    },
    data () {
        return {
            value1: undefined,
            value2: [],
            value3: [],
            treeData: [{
                id: 0,
                label: '一年级',
                children: [{
                    id: 10,
                    label: '语文'
                }, {
                    id: 11,
                    label: '数学'
                }]
            }, {
                id: 1,
                label: '二年级',
                children: [{
                    id: 20,
                    label: '语文'
                }, {
                    id: 21,
                    label: '数学'
                }, {
                    id: 22,
                    label: '英语'
                }]
            }, {
                id: 2,
                label: '三年级',
                children: [{
                    id: 30,
                    label: '语文'
                }, {
                    id: 31,
                    label: '数学'
                }, {
                    id: 32,
                    label: '英语'
                }, {
                    id: 33,
                    label: '自然'
                }]
            }]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
