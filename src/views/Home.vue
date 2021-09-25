<template>
  <div class="page-wrapper">
    <div class="card-wrapper">
      <div class="card-content">
        <h1 class="card-title">
          Get <span>insights</span> that help your business grow.
        </h1>

        <p class="card-summary">
          Discover the benefits of data analytics and make better decisions regarding revenue, customer
          experience, and overall efficiency.
        </p>

        <div class="card-stats">
          <div class="stat-content">
            <p class="stat-number">10k+</p>
            <p class="stat-type">companies</p>
          </div>
          <div class="stat-content">
            <p class="stat-number">314</p>
            <p class="stat-type">templates</p>
          </div>
          <div class="stat-content">
            <p class="stat-number">12m+</p>
            <p class="stat-type">queries</p>
          </div>
        </div>
      </div>

      <div class="card-image"></div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .card-wrapper {
    display: flex;
    align-items: stretch;
    width: 100%;
    max-width: 1110px;
    background: $primaryColor2;
    border-radius: 8px;
    box-shadow: 0 20px 20px -10px rgba(23, 25, 41, 0.203087);

    @media (max-width: 800px) {
      flex-direction: column-reverse;
    }
  }

  .card-content {
    width: 52%;
    padding: 72px 95px 60px 72px;

    @media (max-width: 1000px) {
      padding: 40px 30px 32px;
    }

    @media (max-width: 800px) {
      width: 100%;
      flex-direction: column;
      text-align: center;
    }

    .card-title {
      margin-bottom: 25px;
      font-family: $textFont1;
      font-weight: bold;
      font-size: 36px;
      line-height: 44px;
      color: $neutralColor1;

      @media (max-width: 1000px) {
        font-size: 30px;
        line-height: 36px;
      }

      @media (max-width: 800px) {
        font-size: 28px;
        line-height: 32px;
      }

      span {
        color: $primaryColor3;
      }
    }

    .card-summary {
      font-family: $textFont1;
      font-size: 15px;
      line-height: 25px;
      color: $neutralColor1;
      mix-blend-mode: normal;
      opacity: 0.75;

      @media (min-width: 800px) and (max-width: 1000px) {
        font-size: 14px;
        line-height: 24px;
      }
    }

    .card-stats {
      display: flex;
      margin-top: 72px;

      @media (max-width: 800px) {
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        margin-top: 40px;
      }

      .stat-content {
        color: $neutralColor1;

        &:not(:last-child) {
          margin-right: 60px;

          @media (max-width: 800px) {
            margin-right: 0;
            margin-bottom: 24px;
          }
        }

        .stat-number {
          font-family: $textFont1;
          font-weight: bold;
          font-size: 24px;
          line-height: 29px;

          @media (min-width: 800px) and (max-width: 1000px) {
            font-size: 20px;
            line-height: 25px;
          }
        }

        .stat-type {
          font-family: $textFont2;
          font-size: 12px;
          line-height: 25px;
          letter-spacing: 1px;
          text-transform: uppercase;
          mix-blend-mode: normal;
          opacity: 0.6;

          @media (min-width: 800px) and (max-width: 1000px) {
            font-size: 10px;
            line-height: 23px;
          }
        }
      }
    }
  }

  .card-image {
    position: relative;
    width: 540px;
    border-radius: 0 8px 8px 0;
    background: $primaryColor3;

    @media (max-width: 800px) {
      width: 100%;
      height: 240px;
      border-radius: 8px 8px 0 0;
    }

    &:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;

      background: url('../assets/img/image-header-desktop.jpg') no-repeat center center;
      background-size: cover;
      mix-blend-mode: multiply;
      opacity: 0.75;

      @media (max-width: 800px) {
        background: url('../assets/img/image-header-mobile.jpg') no-repeat top left;
        background-size: cover;
      }
    }
  }
}
</style>
