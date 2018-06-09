<template>
  <div>
    <div class="main-interface">
      <div class="nav-wrapper">
      </div>
      <div class="content-wrapper">
        <div class="items-wrapper">
          <Row>
            <Col span="8">
            <Card>
              <p slot="title">The standard card</p>
              <p>Content of card</p>
              <p>Content of card</p>
              <p>Content of card</p>
            </Card>
            </Col>
            <Col span="8">
            <Card dis-hover>
              <p slot="title">Disable card with hover shadows</p>
              <p>Content of card</p>
              <p>Content of card</p>
              <p>Content of card</p>
            </Card>
            </Col>
            <Col span="8">
            <Card dis-hover>
              <p slot="title">Disable card with hover shadows</p>
              <p>Content of card</p>
              <p>Content of card</p>
              <p>Content of card</p>
            </Card>
            </Col>
          </Row>
  
          <b-navbar toggleable="md" variant="light" class="nav-bar">
            <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
            <b-collapse is-nav id="nav_collapse">
              <b-navbar-nav>
                <b-nav-item href="#">All</b-nav-item>
                <b-nav-item href="#">Physical</b-nav-item>
                <b-nav-item href="#">Virtual</b-nav-item>
              </b-navbar-nav>
              <!-- Right aligned nav items -->
              <b-navbar-nav>
                <b-nav-form>
                  <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search" />
                </b-nav-form>
              </b-navbar-nav>
            </b-collapse>
          </b-navbar>

           <Row>
        <Col span="24">
            <Card>
                <p slot="title">The standard card</p>
                <p>Content of card</p>
            </Card>
        </Col>
        </Row>
                  <Row>
        <Col span="24">
            <Card>
                <p slot="title">The standard card</p>
                <p>Content of card</p>
            </Card>
        </Col>
        </Row>
                  <Row>
        <Col span="24">
            <Card>
                <p slot="title">The standard card</p>
                <p>Content of card</p>
            </Card>
        </Col>
        </Row>
                  <Row>
        <Col span="24">
            <Card>
                <p slot="title">The standard card</p>
                <p>Content of card</p>
            </Card>
        </Col>
        </Row>
        </div>
  
      </div>
  
    </div>
    
  </div>
</template>

<script type="text/ecmascript-6">
  export default {}
</script>

<style lang="stylus" rel="stylesheet/stylus">
.main-interface
    display: flex
    position: absolute
    top: 44px
    bottom: 48px
    width: 100%
    overflow: hidden
    z-index:1
    .nav-wrapper
      flex: 0 0 280px
      width: 80px
      background: #2D4054
      margin-left: 30px
    .content-wrapper
      flex: 1
      .items-wrapper
        padding: 20px 50px 0 30px
          

</style>
