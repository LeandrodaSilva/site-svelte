<script lang="ts">
  function handleClick(evt) {
    let el = evt.target;

    if (el.getAttribute("aria-checked") == "true") {
      el.setAttribute("aria-checked", "false");
      document.querySelector("html").classList.remove("dark")
    } else {
      el.setAttribute("aria-checked", "true");
      document.querySelector("html").classList.add("dark")
    }

  }
</script>

<label>
    <button on:click={handleClick} role="switch" aria-checked="false" class="switch">
        <span>off</span>
        <span>on</span>
    </button>
    Tema
</label>

<style>
  .switch {
    margin: 0;
    padding: 0;
    width: 70px;
    height: 26px;
    border: 2px solid black;
    display: inline-block;
    margin-right: 0.25em;
    line-height: 20px;
    vertical-align: middle;
    text-align: center;
    font: 12px "Open Sans", "Arial", serif;
    pointer-events: all;
  }

  .switch span {
    padding: 0 4px;
    pointer-events: none;
  }

[role="switch"][aria-checked="false"] :first-child,
:global([role="switch"][aria-checked="true"] :last-child) {
  background: #262;
  color: #eef;
}

label {
  user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
  pointer-events: none;
}
</style>
