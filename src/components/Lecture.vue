<template>
  <div class="lecture-detail-container">
    <div class="lecture-detail-container01">
      <div class="lecture-detail-container02">
        <div class="lecture-detail-title" @click="open = !open">
          <span class="lecture-detail-text"> Lecture {{ lecture }}</span>
          <span class="lecture-detail-text01">{{ sign }}</span>
        </div>
      </div>
      <div class="lecture-detail-container03" v-show="open">
        <div class="lecture-detail-container04">
          <span class="lecture-detail-text02">{{ text }}</span>
          <div class="lecture-detail-container05">
            <span>{{ text1 }}</span>
            <span class="lecture-detail-text04">{{ text3 }}</span>
          </div>
          <span class="lecture-detail-text05">{{ text2 }}</span>
        </div>
        <div class="lecture-detail-container06">
          <a
            href="https://www.youtube.com"
            target="_blank"
            rel="noreferrer noopener"
            class="lecture-detail-link"
          >
            <div class="thqLink lecture-detail-watch-now">
              <svg
                viewBox="0 0 877.7142857142857 1024"
                class="lecture-detail-icon"
              >
                <path
                  d="M676.571 512c0 13.143-6.857 25.143-18.286 31.429l-310.857 182.857c-5.714 3.429-12 5.143-18.286 5.143s-12.571-1.714-18.286-4.571c-11.429-6.857-18.286-18.857-18.286-32v-365.714c0-13.143 6.857-25.143 18.286-32 11.429-6.286 25.714-6.286 36.571 0.571l310.857 182.857c11.429 6.286 18.286 18.286 18.286 31.429zM749.714 512c0-171.429-139.429-310.857-310.857-310.857s-310.857 139.429-310.857 310.857 139.429 310.857 310.857 310.857 310.857-139.429 310.857-310.857zM877.714 512c0 242.286-196.571 438.857-438.857 438.857s-438.857-196.571-438.857-438.857 196.571-438.857 438.857-438.857 438.857 196.571 438.857 438.857z"
                ></path>
              </svg>
              <span class="lecture-detail-text06">{{ text4 }}</span>
            </div>
          </a>
          <a
            href="https://www.google.com"
            target="_blank"
            rel="noreferrer noopener"
            class="lecture-detail-link1"
          >
            <div class="thqLink lecture-detail-download">
              <svg
                viewBox="0 0 950.8571428571428 1024"
                class="lecture-detail-icon2"
              >
                <path
                  d="M731.429 768c0-20-16.571-36.571-36.571-36.571s-36.571 16.571-36.571 36.571 16.571 36.571 36.571 36.571 36.571-16.571 36.571-36.571zM877.714 768c0-20-16.571-36.571-36.571-36.571s-36.571 16.571-36.571 36.571 16.571 36.571 36.571 36.571 36.571-16.571 36.571-36.571zM950.857 640v182.857c0 30.286-24.571 54.857-54.857 54.857h-841.143c-30.286 0-54.857-24.571-54.857-54.857v-182.857c0-30.286 24.571-54.857 54.857-54.857h265.714l77.143 77.714c21.143 20.571 48.571 32 77.714 32s56.571-11.429 77.714-32l77.714-77.714h265.143c30.286 0 54.857 24.571 54.857 54.857zM765.143 314.857c5.714 13.714 2.857 29.714-8 40l-256 256c-6.857 7.429-16.571 10.857-25.714 10.857s-18.857-3.429-25.714-10.857l-256-256c-10.857-10.286-13.714-26.286-8-40 5.714-13.143 18.857-22.286 33.714-22.286h146.286v-256c0-20 16.571-36.571 36.571-36.571h146.286c20 0 36.571 16.571 36.571 36.571v256h146.286c14.857 0 28 9.143 33.714 22.286z"
                ></path>
              </svg>
              <span class="lecture-detail-text07">{{ text5 }}</span>
            </div>
          </a>
          <div class="lecture-detail-duration">
            <span class="lecture-detail-text08">{{ duration }}</span>
          </div>
        </div>
        <div class="lecture-detail-container07">
          <span class="lecture-detail-text09">{{ topics }}</span>
        </div>
        <div class="lecture-detail-container08">
          <span class="lecture-detail-text10">{{ text6 }}</span>
        </div>
        <div class="lecture-detail-container09">
          <button class="thqButton lecture-detail-button">{{ button }}</button>
          <button class="thqButton lecture-detail-button1">
            {{ button1 }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LectureDetail",
  data() {
    return {
      open: false,
    };
  },
  props: {
    lecture: {
      type: String,
      default: "Lecture 1",
    },
    button1: {
      type: String,
      default: "PDF",
    },
    text2: {
      type: String,
      default: "Duration:",
    },
    text4: {
      type: String,
      default: "Watch now!",
    },
    text3: {
      type: String,
      default: "Right Click, and Save As",
    },
    text: {
      type: String,
      default: "Watch Online:",
    },
    text6: {
      type: String,
      default: "Transcripts",
    },
    text1: {
      type: String,
      default: "Download:",
    },
    sign: {
      type: String,
      default: "+",
    },
    topics: {
      type: String,
      default:
        "Topics: The Motivation & Applications of Machine Learning, The Logistics of the Class, The Definition of Machine Learning, The Overview of Supervised Learning, The Overview of Learning Theory, The Overview of Unsupervised Learning, The Overview of Reinforcement Learning",
    },
    button: {
      type: String,
      default: "HTML",
    },
    duration: {
      type: String,
      default: "1 hr 9 min",
    },
    text5: {
      type: String,
      default: "Download",
    },
  },
};
</script>

<style scoped>
.lecture-detail-container {
  width: 100%;
  display: flex;
  position: relative;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}
.lecture-detail-container01 {
  flex: 0 0 auto;
  display: flex;
  width: 100%;
  align-items: flex-start;

  padding-right: var(--dl-space-space-halfunit);
  flex-direction: column;
}
.lecture-detail-container02 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  align-items: center;
  grid-row-gap: var(--dl-space-space-unit);
  flex-direction: column;
  justify-content: flex-start;
}
.lecture-detail-title {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  transition: 0.3s;
  align-items: center;
  padding-left: 0px;
  padding-right: 0px;
  flex-direction: row;
  justify-content: space-between;
  background-color: #e0eff2;
}
.lecture-detail-text {
  margin-left: var(--dl-space-space-doubleunit);
}
.lecture-detail-text01 {
  margin-right: var(--dl-space-space-doubleunit);
  padding-right: 0px;
}
.lecture-detail-container03 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  grid-gap: var(--dl-space-space-unit);
  align-items: flex-start;
  padding-top: var(--dl-space-space-unit);
  padding-bottom: var(--dl-space-space-unit);
  flex-direction: column;
}
.lecture-detail-container04 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  align-items: center;
  padding-left: 0px;
  padding-right: 0px;
  flex-direction: row;
  justify-content: space-between;
  background-color: var(--dl-color-gray-900);
}
.lecture-detail-text02 {
  margin-left: var(--dl-space-space-doubleunit);
}
.lecture-detail-container05 {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.lecture-detail-text04 {
  color: red;
  font-size: 14px;
}
.lecture-detail-text05 {
  margin-right: var(--dl-space-space-doubleunit);
}
.lecture-detail-container06 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  align-items: center;
  padding-left: 0px;
  padding-right: 0px;
  flex-direction: row;
  justify-content: space-between;
}
.lecture-detail-link {
  display: contents;
}
.lecture-detail-watch-now {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  margin-left: var(--dl-space-space-doubleunit);
  padding-left: var(--dl-space-space-halfunit);
  padding-right: var(--dl-space-space-halfunit);
  flex-direction: row;
  justify-content: space-between;
  text-decoration: none;
  background-color: red;
}
.lecture-detail-icon {
  fill: var(--dl-color-gray-white);
  width: 36px;
  height: 36px;
  padding-right: var(--dl-space-space-halfunit);
}
.lecture-detail-text06 {
  color: var(--dl-color-gray-white);
  border-color: rgba(0, 0, 0, 0);
  border-width: 1px;
}
.lecture-detail-link1 {
  display: contents;
}
.lecture-detail-download {
  flex: 0 0 auto;
  display: flex;
  align-items: flex-start;
  flex-direction: row;
  justify-content: space-between;
  text-decoration: none;
}
.lecture-detail-icon2 {
  width: 24px;
  height: 24px;
  padding-right: var(--dl-space-space-halfunit);
}
.lecture-detail-text07 {
  padding-left: var(--dl-space-space-halfunit);
}
.lecture-detail-duration {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: center;
}
.lecture-detail-text08 {
  margin-right: var(--dl-space-space-doubleunit);
}
.lecture-detail-container07 {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: flex-start;
}
.lecture-detail-text09 {
  margin-left: var(--dl-space-space-doubleunit);
  margin-right: var(--dl-space-space-doubleunit);
}
.lecture-detail-container08 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  align-items: flex-start;
  flex-direction: row;
  justify-content: flex-start;
  background-color: var(--dl-color-gray-900);
}
.lecture-detail-text10 {
  margin-left: var(--dl-space-space-doubleunit);
}
.lecture-detail-container09 {
  flex: 0 0 auto;
  display: flex;
  align-items: flex-start;
  margin-left: var(--dl-space-space-doubleunit);
  flex-direction: row;
  justify-content: space-between;
}
.lecture-detail-button {
  color: var(--dl-color-gray-white);
  border-color: no;
  margin-right: var(--dl-space-space-unit);
  background-color: var(--dl-color-success-700);
}
.lecture-detail-button1 {
  color: var(--dl-color-gray-white);
  margin-left: var(--dl-space-space-unit);
  background-color: var(--dl-color-success-700);
}
a {
  text-decoration: none;
}
</style>
