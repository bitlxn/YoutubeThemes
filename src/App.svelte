<script lang="ts">
  import BrandTitle from "./components/BrandTitle.svelte";
  import EnableExtension from "./components/EnableExtension.svelte";
  import Footer from "./components/Footer.svelte";
  import Theme from "./components/Theme.svelte";
</script>

<svelte:head>
  <title>Youtube Themes - Main</title>
</svelte:head>

<div class="app" id="app">
  <div class="brandContainer" >
    <BrandTitle title="Youtube Themes" />
  </div>
  <div class="enableContainer">
    <EnableExtension />
  </div>

  <div class="themesContainer">
    <div class="themes" id="themes">
      <Theme name="Original" active={true}/>
      <Theme name="Default+" />
      <Theme name="Discord" />
      <Theme name="Twitch" />
      <Theme name="Reddit" />
      <Theme name="Opera" />
      <Theme name="KDE" />
      <Theme name="Steam" />
      <Theme name="Spotify" />
      <Theme name="Firefox" />
    </div>
  </div>

  <div class="footerContainer">
    <Footer />
  </div>
</div>

<style>
  .app {
    width: 100%;
    color: white;
    outline: none;
    border: transparent;
  }

  .themes {
    text-align: left;
    width: 100%;
    max-height: 315px;
    flex-direction: column;
    justify-content: center;
    overflow-y: scroll;
    align-items: center;
    color: rgba(255, 255, 255, 0.795);
    background: rgba(255, 255, 255, 0.027);
    text-align: center;
  }

  .themesContainer {
    margin: 10px 10px;
    border: 1px solid rgba(255, 255, 255, 0.116);
    border-radius: 5px;
  }

</style>
