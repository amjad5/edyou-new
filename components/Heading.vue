<template>
    <div ref="moving-image" class="jumbotron ">
        <div id="logodiv">
            <a class="text-center">
                <img id="applogo" class="rounded mx-auto d-block" src="/img/edyou+logo+wht.png" alt="Discover Nuxt 3" />
            </a>
        </div>
        <div class="content-jumbo">
            <h1 class="display-4 main-title">
                The ONLY
                college-life app
                you’ll ever need.</h1>
            <p class="lead main-subtitle mt-5">A gated community <span class="font-weight-bold">built exclusively for
                    college students</span>. Connect, share
                experiences, and build lasting relationships.</p>
            <a>
                <img id="appbtn" class="img-thumbnail self-align-left" src="/img/app-store.png" alt="Discover Nuxt 3" />
            </a>
        </div>
        <a id="mobile-app-div" class="d-flex justify-content-end">
            <img id="mobile-app" class="img-thumbnail self-align-left" src="/img/app.png" alt="Discover Nuxt 3" />
        </a>

        <svg viewBox="0 0 1440 319">
            <path fill="#fff" fill-opacity="0"
                d="M0,32L48,80C96,128,192,224,288,224C384,224,480,128,576,90.7C672,53,768,75,864,96C960,117,1056,139,1152,149.3C1248,160,1344,160,1392,160L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
            </path>
        </svg>

    </div>
</template>

<script>
import { ref, onMounted } from 'vue'

// declare a ref to hold the element reference
// the name must match template ref value
const input = ref(null)

onMounted(() => {
//   input.value.focus()
  const handleScroll = () => {
  input.classList.add("useAnimate");
  setScrollY(window.scrollY);
};
})



</script>

<!-- <template>
  <input ref="input" />
</template> -->

<style>

@keyframes slidein {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(100%);
  }
}

.useAnimate {
  animation-name: slidein;
  animation-duration: 500ms;
}


.curved-div svg {
    display: block;
}

#appbtn {
    height: 60px;
    /* width: 100%;  */
    object-fit: contain;
    object-position: 50% 50%;
    overflow: hidden;
    border: none;
    background: none;
    /* left: 0 */
}

#logo-div {
    position: relative;
    z-index: 2;
    width: 100%;
    box-sizing: border-box;
    padding-top: 1.3vw;
    padding-bottom: 1.3vw;
    padding-left: 7vw;
    padding-right: 7vw;
    pointer-events: auto;
}

#applogo {
    width: auto;
    max-width: 100%;
    background: none;
    border: none;
    max-height: 121px;
    overflow: hidden;
}

.jumbotron {
    width: 100vw;
    height: 110vh;
    padding: 1rem;
    background-image: url("~/img/jumbotron-background.jpeg");
    background-size: cover;
    background-position: center;

    mask-image: linear-gradient(to bottom, transparent 0%, black 0%);
    background-attachment: fixed;
    /* <= This one */

    /* Curved corners */
    border-bottom-left-radius: 20% 10%;
    border-bottom-right-radius: 20% 10%;



}

.fadeIn-Delay-2s {
    -webkit-animation-delay: 2s;
    -moz-animation-delay: 2s;
    -o-animation-delay: 2s;
    animation-delay: 2s;
}

.fadeIn-3s {
    -webkit-animation-duration: 3s;
    -moz-animation-duration: 3s;
    -o-animation-duration: 3s;
    animation-duration: 3s;
}

.fadeIn {
    opacity: 0;
    -webkit-animation: fadeIn ease-in 1;
    -moz-animation: fadeIn ease-in 1;
    -o-animation: fadeIn ease-in 1;
    animation: fadeIn ease-in 1;
    -webkit-animation-fill-mode: forwards;
    -moz-animation-fill-mode: forwards;
    -o-animation-fill-mode: forwards;
    animation-fill-mode: forwards;
}

.content-jumbo {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 40%;
    left: 12%;
}

.main-title {
    color: white;
    font-weight: bold;
    font-size: 5rem;
    line-height: 4rem;
}

.main-subtitle {
    color: white;
    font-size: 2rem;
    line-height: 2rem;
}

.thumbnail img {
    text-align: left;
}

#mobile-app {
    height: 90%;
    width: 30%;
    background: none;
    border: none;
    right: 10%;
    bottom: 30%;
}

#mobile-app-div {
    margin-right: 10%;
}
</style>