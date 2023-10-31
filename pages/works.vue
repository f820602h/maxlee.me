<script setup lang="ts">
const { hide } = useLoading();
onMounted(() => {
  window.setTimeout(hide, 500);
});

useHead({
  title: "Works - Max Lee",
  meta: [
    {
      property: "og:title",
      content: "Works - Max Lee",
    },
    {
      name: "twitter:title",
      content: "Works - Max Lee",
    },
  ],
});

const mainWorks = [
  {
    title: "Vue Stage Play",
    description:
      "A component-based package designed to assist you in implementing step-by-step guided tour function within your application.",
    image: "/img/works/stage.png",
    gif: "/img/works/stage.gif",
    link: "https://f820602h.github.io/vue-stage-play/",
    github: "https://github.com/f820602h/vue-stage-play/",
  },
  {
    title: "Vue Surf",
    description:
      "A very customized animated SVG wave Vue component. Adding cool waves to your websites.",
    image: "/img/works/surf.png",
    gif: "/img/works/surf.gif",
    link: "https://f820602h.github.io/vue-surf/",
    github: "https://github.com/f820602h/vue-surf/",
  },
];

const littleWorks = [
  {
    title: "Translate Review Extension",
    description:
      "A browser extension for instant translation, with a reviewable history in a new tab.",
    image: "/img/works/translate.png",
    gif: "",
    link: "https://github.com/f820602h/Translate-Review-Extension",
    github: "https://github.com/f820602h/Translate-Review-Extension",
  },
  {
    title: "Max Blog",
    description:
      "My first blog website was developed using the Hexo framework.",
    image: "/img/works/blog.png",
    gif: "",
    link: "https://maxleebk.com/",
    github: "https://github.com/f820602h/Max-Blog",
  },
  {
    title: "Snaaaaaaake",
    description: "A classic Snake game, developed using Vue 2.",
    image: "/img/works/snake.png",
    gif: "/img/works/snake.gif",
    link: "https://f820602h.github.io/Snaaaaaaake/",
    github: "https://github.com/f820602h/Snaaaaaaake",
  },
  {
    title: "Max-2048",
    description: "A replica of the 2048 game, developed using Vue 3.",
    image: "/img/works/2048.png",
    gif: "/img/works/2048.gif",
    link: "https://f820602h.github.io/Max-2048/",
    github: "https://github.com/f820602h/Max-2048",
  },
  {
    title: "OXGame",
    description: "A Tic-Tac-Toe game developed with vanilla JavaScript.",
    image: "/img/works/ox.png",
    gif: "/img/works/ox.gif",
    link: "https://f820602h.github.io/OXGame/",
    github: "https://github.com/f820602h/OXGame",
  },
  {
    title: "Max Persona",
    description:
      "My first portfolio site was built with jQuery while I was learning front-end development.",
    image: "/img/works/persona.png",
    gif: "/img/works/persona.gif",
    link: "https://f820602h.github.io/Max-Persona/",
    github: "https://github.com/f820602h/Max-Persona",
  },
];
</script>

<template>
  <main class="max-w-1920px mx-auto py-60px px-24px md:px-48px">
    <section class="max-w-900px mx-auto pb-60px">
      <h2
        class="text-32px font-bold italic text-black dark:text-white text-center mb-5"
      >
        Main Project
      </h2>
      <article class="flex justify-between flex-wrap -mx-12px mb-48px">
        <div
          v-for="work in mainWorks"
          :key="work.title"
          class="works relative block w-full md:w-1/2 px-12px mb-24px cursor-pointer group hover:-translate-y-5px duration-550"
        >
          <a :href="work.link" target="_blank" class="">
            <figure
              class="relative w-full rounded overflow-hidden mb-1 duration-550"
            >
              <img class="absolute top-0 left-0 block w-full" :src="work.gif" />
              <img class="image relative z-10 block w-full" :src="work.image" />
            </figure>

            <div class="p-1">
              <h4
                class="text-lg font-bold mb-1 text-gray-700 dark:text-#bbb group-hover:text-black dark:group-hover:text-white duration-350"
                v-text="work.title"
              />
              <p
                class="min-h-40px text-sm text-gray-500 group-hover:text-black dark:group-hover:text-white duration-350"
                v-text="work.description"
              />
            </div>
          </a>

          <a
            :href="work.github"
            target="_blank"
            class="github p-4px text-lg text-gray-600 hover:text-black dark:text-#bbb dark:hover:text-white duration-350"
          >
            <div class="i-iconoir:github" />
          </a>
        </div>
      </article>

      <h2
        class="text-32px font-bold italic text-black dark:text-white text-center mb-5"
      >
        Little Project
      </h2>
      <article class="flex flex-wrap -mx-12px">
        <div
          v-for="work in littleWorks"
          :key="work.title"
          class="works relative block w-full md:w-1/2 px-12px mb-24px cursor-pointer group hover:-translate-y-5px duration-550"
        >
          <a :href="work.link" target="_blank">
            <figure
              class="relative w-full rounded overflow-hidden mb-1 bg-transparent"
            >
              <img class="absolute top-0 left-0 block w-full" :src="work.gif" />
              <img
                class="image relative z-10 block w-full"
                :class="{ freeze: !work.gif }"
                :src="work.image"
              />
            </figure>

            <div class="p-1">
              <h4
                class="text-lg font-bold mb-1 text-gray-700 dark:text-#bbb group-hover:text-black dark:group-hover:text-white duration-350"
                v-text="work.title"
              />
              <p
                class="min-h-40px text-sm text-gray-500 group-hover:text-black dark:group-hover:text-white duration-350"
                v-text="work.description"
              />
            </div>
          </a>

          <a
            :href="work.github"
            target="_blank"
            class="github p-4px text-lg text-gray-600 hover:text-black dark:text-#bbb dark:hover:text-white duration-350"
          >
            <div class="i-iconoir:github" />
          </a>
        </div>
      </article>
    </section>
  </main>
</template>

<style scoped lang="scss">
.works {
  figure {
    filter: grayscale(30%);
    aspect-ratio: 2/1;
    transition: all 0.2s;

    .image {
      opacity: 1;
      transition: all 0.55s;
    }
  }

  .github {
    display: block;
    position: absolute;
    bottom: 50px;
    right: 12px;
    z-index: 15;
  }

  p {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
  }

  &:hover {
    figure {
      filter: grayscale(0%);

      .image:not(.freeze) {
        opacity: 0;
      }
    }
  }
}
</style>