<template>
  <div>
    <b-container class="bg-main shadows-main">
      <p>
        Hello, and welcome to my portfolio. My names Garrett, and as you may
        have guessed I am a web developer. I am currently seeking an entry level Web Developer position.
      </p>

      <p>
        My passions include technology, eSports, mountain biking, and
        <span
          v-b-popover.hover.v-info="
            'Name a coder who doesnt love coffee. Im waiting.'
          "
          >coffee</span
        >. I consider myself self-motivated, fast-learning, highly energetic,
        and adaptable, which I believe makes me compatible with nearly any group
        of people.
      </p>

      <p>
        Over the past two years, I’ve created two eSports organizations, where I
        developed and maintained websites, lead groups of people, connected with
        game developers and broadcasting talent. Both organizations engaged a
        high amount of users and maintained a strong presence across social
        media platforms. You can check them out here: brainscans.net &
        underlords.pro.
      </p>

      <p>
        <em>Why should you hire me?</em> Because I get stuff done, bring
        projects to life, meet deadlines, and am generally fun to be around. And
        I have the experience to show for it.
      </p>
    </b-container>
  </div>
</template>

<script>

export default {

};
</script>

<style scoped></style>
