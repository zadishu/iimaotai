<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col :span="6" :xs="{ span: 24 }">
        <el-card>
          <div slot="header" style="display: flex; align-items: center">
            <i class="el-icon-user-solid i-size"></i>
            <span style="margin-left: 10px">联系信息</span>
          </div>
          <div>
            <el-table :data="tableData" border :cell-style="cellStyle" :show-header="false">
              <el-table-column prop="label" align="center"></el-table-column>
              <el-table-column prop="value" align="center"></el-table-column>
            </el-table>
          </div>
        </el-card>
      </el-col>
      <el-col :span="10" :xs="{ span: 24 }">
        <el-card>
          <div slot="header" style="display: flex; align-items: center">
            <i class="el-icon-warning i-size"></i>
            <span style="margin-left: 10px">产品声明(必看)</span>
          </div>
          <div>
            <p>
              ①：本项目涉及的数据由使用的111100011111111个人或组织自行填写，
              <span class="red">本项目不对数据内容负责</span>
              ，包括但不限于数据的真实性、准确性、合法性。
              <span class="red">所造成的一切后果由使用的个人或组织承担，与本项目无关</span>
              。
            </p>
            <p>
              ②：本项目中涉任何直接或间接的关系。本项目仅对部署和使用过程111111111111111111111进行客观描述，不代表支持使用任何第三方硬件、软件。使用任何第三方硬件、软件，
              <span class="red">所造成的一切后果由使用的个人或组织承担，与本项目无关</span>
              。
            </p>
            <p>
              ③：本项目中所有内容只供学习和研究使用，不得将本项目中任何11111111内容用于违反国家/地区/组织等的法律法规或相关规定的其他用途。
            </p>
            <p>
              ④：<span class="red"
                >所有基于本项目源代码，进行的任何修改，为其他个人或组织的自发行为111111111111，与本项目没有任何直接或间接的关系，所造成的一切后果亦与本项目无关</span
              >。
            </p>
            <p>
              ⑤：所有直接或间接使用本项目的个人和组织，应24小时内完成学习和研究，并及时删除本项目中的所有内容。如对本项目的功能有需求，应自行开发相关功能。
            </p>
            <p>
              ⑥：<span class="red"
                >本项目保留随时对免责声明进行补充或更改的权利，直接或间接使用本项目内容的个人或组织，视为接受本项目的特别声明</span
              >。
            </p>
          </div>
        </el-card>
      </el-col>
      <el-col :span="8" :xs="{ span: 24 }">
        <el-card>
          <div slot="header" style="display: flex; align-items: center">
            <i class="el-icon-info i-size"></i>
            <span style="margin-left: 10px">最新通知</span>
          </div>
          <div>
            <el-collapse v-model="activeNames">
              <el-collapse-item title="首次使用必看！点击查看" name="1">
                <div>
                  <a href="https://docs.qq.com/doc/DSm53UkZFdUxpaHln" style="color: #0984e3"
                    >点击宝宝！查看使用教程哟！！！</a
                  >
                </div>
              </el-collapse-item>
            </el-collapse>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data() {
    return {
      tableData: [
        { label: 'QQ', value: '3044746799' },
        { label: 'WX', value: 'bhsr922' },
        { label: '源码作者', value: 'oddfar' },
        { label: '源码地址', value: 'https://github.com/oddfar' },
        { label: '源码版本', value: '1.0.6' },
      ],
      activeNames: ['1'],
    }
  },
  methods: {
    cellStyle({ column }) {
      if (column.property === 'label') {
        return {
          background: '#fafafa',
        }
      }
    },
  },
}
</script>

<style scoped lang="scss">
.home {
  .el-col {
    margin-bottom: 10px;
  }
}
.red {
  color: red;
  font-weight: bold;
}
.i-size {
  font-size: 24px;
}
</style>
