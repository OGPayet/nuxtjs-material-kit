<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="header != '' ? `background-image: url(${header})` : `background-image: url(${require('@/assets/img/city-profile.jpg')})`"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="require('@/assets/img/faces/christian.jpg')"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Carla Hortensia</h3>
                  <h6>Designer</h6>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple md-dribbble"
                    ><i class="fab fa-dribbble"></i
                  ></md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple md-twitter"
                    ><i class="fab fa-twitter"></i
                  ></md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple md-pinterest"
                    ><i class="fab fa-pinterest"></i
                  ></md-button>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              An artist of considerable range, Chet Faker — the name taken by
              Melbourne-raised, Brooklyn-based Nick Murphy — writes, performs
              and records all of his own music, giving it a warm, intimate feel
              with a solid groove structure.
            </p>
          </div>
          <div class="profile-tabs">
            <tabs
              :tab-name="['Studio', 'Work', 'Favorite']"
              :tab-icon="['camera', 'palette', 'favorite']"
              plain
              nav-pills-icons
              color-button="success"
            >
              <!-- here you can add your content for tab-content -->
              <template slot="tab-pane-1">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="require('@/assets/img/examples/studio-1.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/studio-2.jpg')" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="require('@/assets/img/examples/studio-5.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/studio-4.jpg')" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="require('@/assets/img/examples/olu-eletu.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/clem-onojeghuo.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/cynthia-del-rio.jpg')" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="require('@/assets/img/examples/mariya-georgieva.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/clem-onojegaw.jpg')" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-3">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="require('@/assets/img/examples/mariya-georgieva.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/studio-3.jpg')" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="require('@/assets/img/examples/clem-onojeghuo.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/olu-eletu.jpg')" class="rounded" />
                    <img :src="require('@/assets/img/examples/studio-1.jpg')" class="rounded" />
                  </div>
                </div>
              </template>
            </tabs>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
export default {
  components: {
    Tabs
  },
  bodyClass: "profile-page",
  props: {
    header: {
      type: String,
      default: '',
    },
    img: {
      type: String,
      default: '',
    }
  },
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}

.profile-tabs::v-deep {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
