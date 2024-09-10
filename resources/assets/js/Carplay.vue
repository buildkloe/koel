<template>
  <div>
    <div>Car play</div>
    <div class="plyr" >
      <audio controls crossorigin="anonymous" src="/play/03b0d869-bf30-4116-aac2-341f9d8661a3?t=104|GUn78Y19cMPzSxhOvz6G4ZKgaoPxD3PGlg3ulcOO" title="李健 - 向往"></audio>
    </div>
  </div>
</template>

<script lang="ts" setup>
import plyr from 'plyr'

const plyrWrapper = document.querySelector<HTMLElement>('.plyr')
const player = plyr.setup(plyrWrapper, { controls: [] })[0]

</script>

<style lang="scss">
@import "#/app.scss";

#dragGhost {
  display: inline-block;
  background: var(--color-green);
  padding: .8rem;
  border-radius: .3rem;
  color: var(--color-text-primary);
  font-family: var(--font-family);
  font-size: 1rem;
  font-weight: var(--font-weight-light);
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;

  @media (hover: none) {
    display: none;
  }
}

#copyArea {
  position: absolute;
  left: -9999px;
  width: 1px;
  height: 1px;
  bottom: 1px;

  @media (hover: none) {
    display: none;
  }
}

#main {
  display: flex;
  height: 100vh;
  flex-direction: column;
  justify-content: flex-end;
}

#main {
  @media screen and (max-width: 768px) {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    padding-top: var(--header-height);
  }
}
</style>
