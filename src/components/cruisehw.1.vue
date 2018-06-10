<template>
  <div class="layout">
    <Layout>
      <Sider breakpoint="md" hide-trigger class="sider" width="220">
        <Menu active-name="1-2" width="auto" :open-names="['1']" class="nav-menu">
          <MenuItem name="1">
          <span class="icon-dashboard"></span> DASHBOARD
          </MenuItem>
          <MenuItem name="2">
          <span class="icon-sitemap"></span> AGENT
          </MenuItem>
          <MenuItem name="3">
          <span class="icon-boat"></span> MY CRUISE
          </MenuItem>
          <MenuItem name="4">
          <span class="icon-life-bouy"></span> HELP
          </MenuItem>
          <div class="history-record">
            <h4 class="history-title">History</h4>
            <ul class="history-items">
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
              <li type="disc">bjstdmngbgr02/Acceptance_test</li>
            </ul>
          </div>
        </Menu>
      </Sider>
      <Layout class="content-wrapper">
        <Row class="overview">
          <Col span="8">
          <div id="wrap-building">
          <Card class="building-card">
            <Row>
              <Col span="8"><strong>Building</strong></Col>
            </Row>
            <Row>
              <Col span="2" class="building-number"><strong>3</strong></Col>
            </Row>
          </Card>
          </div>
          </Col>
          <Col span="8">
          <div id="wrap-idle">
          <Card class="idle-card">
            <Row>
              <Col span="8"><strong>Idle</strong></Col>
            </Row>
            <Row>
              <Col class="idle-number" span="2"><strong>5</strong></Col>
            </Row>
          </Card>
          </div>
          </Col>
          <Col span="8">
          <Card class="status-card">
            <Row>
              <Col align="center" span="8">ALL</Col>
              <Col align="center" span="8">PHYSICAL</Col>
              <Col align="center" span="8">VIRTUAL</Col>
            </Row>
            <Row>
              <Col align="center" span="8">8</Col>
              <Col align="center" span="8">4</Col>
              <Col align="center" span="8">4</Col>
            </Row>
          </Card>
          </Col>
        </Row>
          <Menu mode="horizontal" active-name="1">
            <MenuItem name="1"> All
            </MenuItem>
            <MenuItem class="phy-tab" name="2"> Physical
            </MenuItem>
            <MenuItem class="vir-tab" name="3"> Virtual
            </MenuItem>  
            <Row type="flex" justify="center" align="middle">
              <Col span="12" >
            <b-nav-form class="search-tab">
              <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search" />
            </b-nav-form>
           </Col>
                <Col span="1">
              <span class="icon-th-card" ></span></Col>
              <Col>
              <span class="icon-th-list"></span></Col></Row>
          </Menu>
        <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img height="80" width="80" src="../assets/windows.png" />
              </Col>
              <Col>
              <Row>
                <Col>
                <span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button size="small" class="machine-status-idle">idle</Button>
                <span class="icon-info"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" v-for="(i, index) in resources" :key="index">{{i}}
                  <span class="icon-trash" @click="()=>deleteRes(i)"></span>
                </Tag>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row>
        <!-- <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img src="../assets/windows.png" />
              </Col>
              <Col>
              <Row>
                <Col><span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button class="machine-status-warning" type="warning" size="small">warning</Button>
                <span class="icon-info icon-info-warning"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" v-for="(i,index) in resources" :key="index">{{i}}
                  <span class="icon-trash" @click.stop.prevent="deleteRes(i)"></span>
                </Tag>
                <Button class="deny-btn" size="small"><span class="icon-deny"></span>Deny</Button>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row> -->
               <!-- <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img src="../assets/ubuntu.png" />
              </Col>
              <Col>
              <Row>
                <Col><span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button class="machine-status-warning" type="warning" size="small">warning</Button>
                <span class="icon-info icon-info-warning"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" v-for="(i,index) in resources" :key="index">{{i}}
                  <span class="icon-trash" @click.stop.prevent="deleteRes(i)"></span>
                </Tag>
                <Button class="deny-btn" size="small"><span class="icon-deny"></span>Deny</Button>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row> -->
                <!-- <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img src="../assets/debin.png" />
              </Col>
              <Col>
              <Row>
                <Col><span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button class="machine-status-warning" type="warning" size="small">warning</Button>
                <span class="icon-info icon-info-warning"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" v-for="(i,index) in resources" :key="index">{{i}}
                  <span class="icon-trash" @click.stop.prevent="deleteRes(i)"></span>
                </Tag>
                <Button class="deny-btn" size="small"><span class="icon-deny"></span>Deny</Button>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row> -->
        <!-- <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img height="80" width="80" src="../assets/suse.png" />
              </Col>
              <Col>
              <Row>
                <Col>
                <span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button size="small" class="machine-status-idle">idle</Button>
                <span class="icon-info"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" :resouces="resources" v-for="(i,index) in resources" :key="index">{{i}}
                  <span class="icon-trash" @click="deleteRes(i)"></span>
                </Tag>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row> -->
        <windows1></windows1>
        <windows2></windows2>
        <ubuntu></ubuntu>
        <debin></debin>
        <suse></suse>
        <centos></centos>
        <!-- <Row class="machine-item">
          <Col span="24">
          <Card>
            <Row gutter="230">
              <Col span="2">
              <img height="80" width="80" src="../assets/cent_os.png" />
              </Col>
              <Col>
              <Row>
                <Col>
                <span class="icon-desktop"></span>
                <span class="machine-address">bjstdmngbgr01.thoughtworks.com</span>
                <Button size="small" class="machine-status-idle">idle</Button>
                <span class="icon-info"></span>
                <span class="machine-ip">192.168.1.102</span>
                <span class="icon-folder"></span>
                <span>/var/lib/cruise-agent</span>
                </Col>
                <Col class="explorer-wrapper">
                <b-btn size="sm" class="add" v-b-modal.modalPrevent><span class="icon-plus"></span></b-btn>
                <Tag class="resources" v-for="(i,index) in resources" :key="index"> {{i}}
                  <span class="icon-trash" @click="deleteRes(i)"></span>
                </Tag>
                </Col>
              </Row>
              </Col>
            </Row>
          </Card>
          </Col>
        </Row> -->
         <b-modal id="modalPrevent"
             ref="modal"
             @ok="handleOk"
             @shown="clearName">
      <form @submit.stop.prevent="handleSubmit">
        <b-form-input type="text"
                      placeholder="e.g. Chrome"
                      v-model="inputRes"></b-form-input>
      </form>
    </b-modal>
      </Layout>
    </Layout>
  </div>
</template>

<script>
import centos from './centos'
import suse from './suse'
import debin from './debin'
import windows1 from './windows1'
import windows2 from './windows2'
import ubuntu from './ubuntu'

export default {
  props: {
    inputRes: {
      type: String
    }
  },
  data () {
    return {
      resources: ['Chrome', 'Safari', 'Ubuntu', 'Firefox'],
      resourceCounter: 4,
      inputRes: ''
    }
  },
  methods: {
    deleteRes (x) {
      for (let i = 0; i < this.resources.length; i++) {
        if (this.resources[i] === x) {
          this.resources.splice(i, 1)
        }
      }
    },
    clearName () {
      this.inputRes = ''
    },
    handleOk (evt) {
      evt.preventDefault()
      if (!this.inputRes) {
        alert('Please input explorer name')
      } else {
        this.handleSubmit()
      }
    },
    handleSubmit () {
      this.resources.push(this.inputRes)
      this.clearName()
      this.$refs.modal.hide()
    }
  },
  components: {
    centos,
    debin,
    suse,
    ubuntu,
    windows1,
    windows2
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "../common/stylus/variable"
  .layout
    border: 1px solid #d7dde4
    position: relative
    border-radius: 4px
    overflow: hidden
    padding-bottom: 12px
    .sider
      background: #2D4054
      z-index: 0
    .content-wrapper
      padding: 12px 48px 0 24px
    .ivu-layout
      background: #F3F3F3
      .ivu-menu-vertical .ivu-menu-item:hover, .ivu-menu-vertical .ivu-menu-submenu-title:hover
        background: #435466
        color: #00B4CF
      .ivu-menu-light.ivu-menu-vertical .ivu-menu-item-active:not(.ivu-menu-submenu)
        color: #00B4CF
      .ivu-menu-light.ivu-menu-horizontal .ivu-menu-item-active, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-item:hover, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu-active, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu:hover
        color: #00B4CF
        border-bottom: 3px solid #00B4CF
      .nav-menu
        background: #2D4054
        color: #fff
      .overview
        margin: 12px 0
        .building-head
          font-size: 28px bold 
        .building-card
          margin-right: 12px
          background-color: #FF9A2A
          color:#fff
          position: relative
          z-index: 1
      
          .building-number
            float: right
        .idle-card
          margin: 0 12px
          color:#fff
          background-color: #7FBC39
          .idle-number
            float: right
        .status-card
          margin-left: 12px
      .phy-tab
        border-left: 1px solid #E1E4E6
      .vir-tab
        border-left: 1px solid #E1E4E6
        border-right: 1px solid #E1E4E6
      .icon-th-list
        color: #00B4CF
      .machine-item
        margin: 12px 0
        .icon-desktop
          font-size: 16px
        .machine-address
          padding:0 20px
        .machine-status-idle
          padding:0 20px
          background-color:#7FBC39
          color:#fff
        .icon-info
          padding-left: 105px
          font-size: 16px
        .machine-ip
          padding: 0 20px
        .icon-folder
          font-size: 16px
          padding: 0 20px
        .explorer-wrapper
          padding-top: 30px
          .add
           background: #00B4CF
           border: #00B4CF
           color: #fff
           font-size: 10px
          .resources
            background-color: #EFEFEF
            font-size: 14px
            font-family: Avenir, Helvetica, Arial, sans-serif
            .icon-trash
              padding-left: 8px
              font-size: 16px
          .deny-btn
            float: right
            background: #00B4CF
            color: #fff
        .machine-status-warning
          padding: 0 20px
        .icon-info-warning
          padding-left: 80px
  .history-record
    padding: 480px 0 0 20px
    color: #999
    font-size: 12px
    overflow: hidden
    .history-title
      font-size: 24px

#wrap-building:after
  content: '\f013'
  font-family: cruise
  font-style: normal
  font-weight: normal
  color: #fff
  position: absolute
  font-size: 85px
  top: 50%
  left: 50%
  margin: -65px 0 0 -50px
  z-index: 2
  overflow: hidden
  opacity: .4


#wrap-idle:after
  content: "\f0f4" 
  font-family: cruise
  font-style: normal
  font-weight: normal
  color: #fff
  position: absolute
  font-size: 85px
  top: 50%
  left: 50%
  margin: -65px 0 0 -50px
  z-index: 2
  overflow: hidden
  opacity: .4   
</style>
