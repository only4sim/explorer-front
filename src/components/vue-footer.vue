<style lang="scss" scoped>
.vue-footer {
  flex-shrink: 0;
  width: 100%;
  color: #333333;
  background: #f5f6fa;

  @include media("<=desktop") {
    padding: 1rem;
  }

  @include media(">desktop") {
    padding-top: 4rem;
    padding-bottom: 2rem;
  }

  .logo {
    width: 150px;
    height: auto;
    margin-top: -2rem;

    @include media("<=desktop") {
      margin-top: 1rem;
      margin-bottom: 1rem !important;
    }
  }

  h5 {
    font-size: 18px;
    font-weight: bold;
  }

  small {
    color: #666666;
    font-size: 12px;
  }

  li {
    margin: 1rem 0;

    a {
      color: #333333;
      font-size: 15px;
    }
  }

  .nav-links {
    @include media("<=desktop") {
      padding-top: 1rem;
    }
  }

  .explorer {
    position: relative;

    small.top {
      position: absolute;
      top: -1.5rem;

      @include media("<=desktop") {
        top: -0.1rem;
      }
    }
  }

  .download {
    display: flex;
    flex-direction: column;
    align-items: center;

    @include media("<=desktop") {
      margin: 0 auto;
    }

    .title {
      margin-bottom: 1rem;

      @include media("<=desktop") {
        margin-bottom: 0;
      }
    }

    .links {
      @include media("<=desktop") {
        display: flex;
        align-items: center;
      }

      a {
        margin: 0.5rem 0;
        display: block;
        img {
          display: block;
          margin: 0 auto;

          &.appstore {
            width: 130px;
            height: auto;
          }

          &.google-play {
            width: 150px;
            height: auto;
          }
        }
      }
    }

    .copyright {
      margin-top: 1rem;

      @include media("<=desktop") {
        margin-top: 0;
      }
    }
  }
}
</style>
<template>
  <footer class="vue-footer border-top">
    <div class="container">
      <div class="row">
        <div class="col-12 col-lg">
          <img
            class="mb-2 logo"
            src="/static/img/nebulas-logo.png"
            alt="nebulas"
          />
        </div>
        <div class="col-6 col-lg explorer nav-links">
          <small class="top">Nebulas Ecosystem</small>

          <h5>Explorer</h5>
          <small>Blockchain, dStaking</small>
          <ul class="list-unstyled text-small">
            <li>
              <router-link :to="'/blocks'">
                {{ $t("headerBlocksSubmenu") }}
              </router-link>
            </li>
            <li>
              <router-link :to="'/blocks'">
                {{ $t("headerTransactionsSubmenu") }}
              </router-link>
            </li>
            <li>
              <a
                href="https://github.com/nebulasio/explorer/issues"
                target="__blank"
                >Submit Issues</a
              >
            </li>
          </ul>
        </div>
        <div class="col-6 col-lg nav-links">
          <h5>Nodes</h5>
          <small>PoD Consensus</small>
          <ul class="list-unstyled text-small">
            <li>
              <a target="__blank" href="https://node.nebulas.io/list">Nodes</a>
            </li>
            <li>
              <a target="__blank" href="https://node.nebulas.io/govern"
                >Governance</a
              >
            </li>
            <li>
              <a
                target="__blank"
                href="https://wiki.nebulas.io/en/latest/node-strategy/README.html"
                >Node Help</a
              >
            </li>
          </ul>
        </div>
        <div class="col-6 col-lg nav-links">
          <h5>Go.nebulas</h5>
          <small>Community Collaboration </small>
          <ul class="list-unstyled text-small">
            <li>
              <a target="__blank" href="https://go.nebulas.io/projects"
                >Projects</a
              >
            </li>
            <li>
              <a target="__blank" href="https://go.nebulas.io/proposals"
                >Proposals</a
              >
            </li>
            <li>
              <a
                target="__blank"
                href="https://www.notion.so/Go-nebulas-io-Help-Documentation-cbdeb02e0ff547b2b7cf59f2d249aafb"
                >Go Nebulas Help</a
              >
            </li>
          </ul>
        </div>

        <div class="col-6 col-lg nav-links">
          <h5>nebulas.io</h5>
          <ul class="list-unstyled text-small">
            <li>
              <a target="__blank" href="https://nebulas.io/wallets.html"
                >Wallets</a
              >
            </li>
            <li>
              <a
                target="__blank"
                href="https://wiki.nebulas.io/en/latest/go-nebulas/blockchain/mainnet.html"
                >Documents</a
              >
            </li>
            <li>
              <a target="__blank" href="https://community.nebulas.io/">Forum</a>
            </li>
          </ul>
        </div>

        <div class="col-6 col-lg download">
          <small class="title">Nas nano pro Download</small>

          <div class="links">
            <a
              href=" https://itunes.apple.com/us/app/nas-nano-pro/id1441776793&mt=8"
              target="__blank"
            >
              <img
                class="appstore"
                src="/static/img/download-on-the-appstore.png"
              />
            </a>
            <a
              href=" https://play.google.com/store/apps/details?id=io.nebulas.wallet.android&hl=en_US"
              target="__blank"
            >
              <img
                class="google-play"
                src="/static/img/get-it-on-google-play.png"
              />
            </a>
          </div>

          <small class="copyright">Copyright 2017 - 2020</small>
        </div>
      </div>
    </div>
  </footer>
</template>
