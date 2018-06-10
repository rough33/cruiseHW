<template>
<div>
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
                <b-btn size="sm" class="add" v-b-modal.modalPrevent1><span class="icon-plus"></span></b-btn>
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
        <b-modal id="modalPrevent1"
             ref="modal"
             @ok="handleOk"
             @shown="clearName">
      <form @submit.stop.prevent="handleSubmit">
        <b-form-input type="text"
                      placeholder="e.g. Chrome,Firefox"
                      v-model="inputRes"></b-form-input>
      </form>
    </b-modal>
    </div>
</template>

<script>
export default {
  props: {
    inputRes: {
      type: String
    }
  },
  data () {
    return {
      resources: ['Chrome', 'Safari', 'Ubuntu', 'Firefox'],
      resourceCounter: 4
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
      if (this.inputRes.indexOf(',') > -1) {
        var inputReses = this.inputRes.split(',')
        for (let i = 0; i < inputReses.length; i++) {
          this.resources.push(inputReses[i])
        }
      } else {
        this.resources.push(this.inputRes)
      }
      this.clearName()
      this.$refs.modal.hide()
    }
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
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
</style>
