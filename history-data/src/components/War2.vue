<template>
  <div>
    <div class="title">第二次世界大战时期各国关系图</div>
    
  <el-table
    :header-cell-style="{background:'#eef1f6',color:'#606266'}"
    :data="tableData"
    border
    width="500"
    >
    <el-table-column
      prop="country"
      align="center"
      label="国家"
      >
    </el-table-column>
        <el-table-column prop="withChina" align="center" label="中国-China"  >
            <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withChina }}</p>
                <p>住址: {{ scope.row.withChina }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withChina==0" src="../assets/friends.png" style="width: 30px;height: 30px">
                  <img v-if="scope.row.withChina==1" src="../assets/enemy.png" style="width: 30px;height: 30px">
                  <img v-if="scope.row.withChina==2" src="../assets/complicated.png" style="width: 30px;height: 30px">
                </div>
              </el-popover>
            </template>
        </el-table-column>

        <el-table-column prop="withUSA" label="美国-America"  align="center" >
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withUSA }}</p>
                <p>住址: {{ scope.row.withUSA }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withUSA==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withUSA==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withUSA==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column prop="withUK" label="英国-England"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withUK }}</p>
                <p>住址: {{ scope.row.withUK }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withUK==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withUK==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withUK==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column
          prop="withRessia" label="俄罗斯-Russia"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withRessia }}</p>
                <p>住址: {{ scope.row.withRessia }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withRessia==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withRessia==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withRessia==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column prop="withJapan" label="日本-Japan"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withJapan }}</p>
                <p>住址: {{ scope.row.withJapan }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withJapan==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withJapan==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withJapan==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column prop="withItaly" label="意大利-Italy"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withItaly }}</p>
                <p>住址: {{ scope.row.withItaly }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withItaly==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withItaly==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withItaly==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column prop="withFrance" label="法国-France"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withFrance }}</p>
                <p>住址: {{ scope.row.withFrance }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withFrance==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withFrance==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withFrance==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

        <el-table-column prop="withGermany" label="德国-Germany"  align="center">
          <template slot-scope="scope">
              <el-popover trigger="hover" placement="top">
                <p>姓名: {{ scope.row.withGermany }}</p>
                <p>住址: {{ scope.row.withGermany }}</p>
                <div slot="reference" >
                  <img v-if="scope.row.withGermany==0" src="../assets/friends.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withGermany==1" src="../assets/enemy.png" style="width: 30px; height: 30px">
                  <img v-if="scope.row.withGermany==2" src="../assets/complicated.png" style="width: 30px; height: 30px">
                </div>
              </el-popover>
          </template>
        </el-table-column>

  </el-table>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        tableData: [{
          country: '中国',
          withChina: -1,
          withUSA: 0,
          withUK: 0,
          withRessia: 0,
          withJapan: 1,
          withItaly:1,
          withFrance:0,
          withGermany:1,
        },{
          country: '美国',
          withChina: 0,
          withUSA: -1,
          withUK: 0,
          withRessia: 0,
          withJapan: 1,
          withItaly:1,
          withFrance:0,
          withGermany:1,
        },{
          country: '英国',
          withChina: 0,
          withUSA: 0,
          withUK: -1,
          withRessia: 0,
          withJapan: 1,
          withItaly:1,
          withFrance:0,
          withGermany:1,
        },{
          country: '俄罗斯',
          withChina: 0,
          withUSA: 0,
          withUK: 0,
          withRessia: -1,
          withJapan: 1,
          withItaly:1,
          withFrance:0,
          withGermany:1,
        },{
          country: '日本',
          withChina: 1,
          withUSA: 1,
          withUK: 1,
          withRessia: 1,
          withJapan: -1,
          withItaly:0,
          withFrance:1,
          withGermany:0,
        },{
          country: '意大利',
          withChina: 1,
          withUSA: 1,
          withUK: 1,
          withRessia: 1,
          withJapan: 0,
          withItaly:-1,
          withFrance:1,
          withGermany:0,
        },{
          country: '法国',
          withChina: 0,
          withUSA: 0,
          withUK: 0,
          withRessia: 0,
          withJapan: 1,
          withItaly:1,
          withFrance:-1,
          withGermany:1,
        },{
          country: '德国',
          withChina: 1,
          withUSA: 1,
          withUK: 1,
          withRessia: 1,
          withJapan: 0,
          withItaly:0,
          withFrance:1,
          withGermany:-1,
        }
        ]
      }
    }
  }
</script>

<style >
.title{
  font-size: 24px;
  font-weight: bolder;
  text-align: center;
  margin-bottom: 10px;
}
</style>