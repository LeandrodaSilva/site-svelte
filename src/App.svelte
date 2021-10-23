<script lang="ts">
  import Layout from "./Layout.svelte";
  import Switch from "./components/Switch.svelte";
  export let name: string;
</script>

<Layout>
  <h1>{name}</h1>
  <Switch />
  <section class="headingMd padding1px">
    <h2 class="headingLg">Contato</h2>
    <ul class="list">
      <li class="listItem">
        <svg class="icon">
          <use xlink:href="/svgs/regular.svg#envelope" />
        </svg>
        <a href="mailto:ld_silva13@hotmail.com?subject=Olá%20Leandro">
          me@leandrodasilva.dev
        </a>
      </li>

      <li class="listItem">
        <svg class="icon">
          <use xlink:href="/svgs/brands.svg#github" />
        </svg>
        <a href="https://github.com/LeandrodaSilva">LeandroDaSilva</a>
      </li>

      <li class="listItem">
        <svg class="icon">
          <use xlink:href="/svgs/brands.svg#keybase" />
        </svg>
        <a href="https://keybase.io/ldsilva">ldsilva</a>
      </li>
    </ul>
  </section>
</Layout>

<style>
  h1 {
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
    display: none;
  }

  .listItem {
    display: flex;
  }

  .listItem a {
    margin-left: 5px;
  }

  .icon {
    height: 32px;
    width: 32px;
  }
</style>
