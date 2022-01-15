<template>
  <div class="">
    <div class="appbar-desktop d-none d-lg-block border-bottom py-3">
      <b-navbar variant="faded" type="light" toggleable="lg">

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        
        <b-navbar-brand class="mb-0">
            <span style="font-size: 20px; font-weight: 700">
                Sneakers
            </span>
        </b-navbar-brand>

        <b-collapse id="nav-collapse" is-nav class="">
          <b-navbar-nav>
            <b-nav-item class="">
              <div class="px-2">
                <span class="text-muted">
                  Collections
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div class="px-2">
                <span class="text-muted">
                  Men
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div class="px-2">
                <span class="text-muted">
                  Women
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div class="px-2">
                <span class="text-muted">
                  About
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div class="px-2">
                <span class="text-muted">
                  Contact
                </span>
              </div>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>

        <b-navbar-nav class="ml-auto d-flex flex-row align-items-center">
          <b-nav-item class="col-6">
            <span>
              <!-- <i class="fas fa-shopping-cart"></i> -->
              <b-img src="/assets/icon-cart.svg" alt=""></b-img>
            </span>
          </b-nav-item>
          <b-nav-item class="col-6">
            <span>
              <b-img src="./assets/image-avatar.png" class="avatar" rounded="circle" alt="Circle image" height="40px"></b-img>
            </span>
          </b-nav-item>
        </b-navbar-nav>

      </b-navbar>
    </div>

    <div class="appbar-mobile d-lg-none d-md-block">
      <b-navbar variant="faded" type="light" toggleable="lg">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-navbar-brand tag="h1" class="mb-0">BootstrapVue</b-navbar-brand>
        
        <b-navbar-nav class="ml-auto d-flex flex-row justify-content-between align-items-center">
          <b-nav-item class="col-6">
            <span>
              <i class="fas fa-shopping-cart"></i>
            </span>
          </b-nav-item>
          <b-nav-item class="col-6">
            <span>
              <b-img src="./assets/user.jpg" rounded="circle" alt="Circle image" height="35px"></b-img>
            </span>
          </b-nav-item>
        </b-navbar-nav>
        
        <b-collapse id="nav-collapse" is-nav class="">
          <b-navbar-nav>
            <b-nav-item class="">
              <div>
                <span class="text-muted">
                  Collections
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div>
                <span class="text-muted">
                  Men
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div>
                <span class="text-muted">
                  Women
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div>
                <span class="text-muted">
                  About
                </span>
              </div>
            </b-nav-item>
            <b-nav-item>
              <div>
                <span class="text-muted">
                  Contact
                </span>
              </div>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    
    
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  props: {

  }
}
</script>
<style scoped>

.avatar:hover {
    border: 2px solid hsl(26, 100%, 55%) !important;
}
</style>