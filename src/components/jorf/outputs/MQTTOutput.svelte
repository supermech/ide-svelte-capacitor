<script>
  import Output from "./Output.svelte";
  import VariableInserter from "@components/VariableInserter.svelte";

  export let params = { to: "", topic: "", content: "" };

  export function summary() {
    return "MQTT push to...";
  }
  function test() {
    console.log("testing MQTT push to " + params.url);
  }
</script>

<Output {test}>
  <label class="input-group ml-2 mb-2">
    <span>To</span>
    <input
      type="text"
      placeholder="broker URL"
      class="input input-bordered"
      bind:value={params.to}
    />
  </label>
  <label class="input-group ml-2 mb-2">
    <span>topic</span>
    <input
      type="text"
      placeholder="#home"
      class="input input-bordered"
      bind:value={params.topic}
    />
  </label>
  <label class="input-group ml-2 mb-2">
    <span>Content</span>
    <input
      type="text"
      placeholder=""
      class="input input-bordered"
      bind:value={params.content}
    />
  </label>
  <!-- <div class="indicator-item pt-6">
      <VariableInserter />
    </div> -->
</Output>
