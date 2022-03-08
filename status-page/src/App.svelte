<svelte:options tag="status-page" />

<script>
  import { onMount } from "svelte";

  import Title from "./Title.svelte";
  import LightBulb from "./LightBulb.svelte";
  import PlannedMaintennance from "./PlannedMaintenance.svelte";
  import DateDisplay from "./DateDisplay.svelte";

  export let href = "https://reqres.in/api/users?page=2";
  let data = {
    tenant: "Customer1",
    incidents: [
      {
        id: "1",
        date: "1646747445",
        level: "high",
        state: "planned",
        description: "Deploy new release",
      },
      {
        id: "2",
        date: "1646747445",
        level: "low",
        state: "planned",
        description: "User access investigations",
      },
      {
        id: "3",
        date: "1646747445",
        level: "medium",
        state: "planned",
        description: "Cleanup of files",
      },
      {
        id: "4",
        date: "1646727445",
        level: "high",
        state: "done",
        description: "Atomic bomb dismantling",
      },
      {
        id: "5",
        date: "1646727445",
        level: "medium",
        state: "done",
        description: "Some database update",
      },
    ],
    events: [
      {
        date: "1646727445",
        title: "Planned maintenance",
        description: "Lorem ipsum dolor sit amet",
      },
      {
        date: "1646727445",
        title: "Planned maintenance 2 ",
        description: "Lorem ipsum dolor sit amet too",
      },
    ],
  };

  onMount(async () => {
    // const res = await fetch(href);
    // data = await res.json();
  });
</script>

<div class="container">
  <div class="row">
    <div class="col">
      <Title kommune={data.tenant} />
    </div>
  </div>

  <div class="row">
    <div class="col">
      <LightBulb />
    </div>
    <div class="col">
      <PlannedMaintennance incidents={data.incidents} />
    </div>
    <div class="col">
      <DateDisplay events={data.events} />
    </div>
  </div>
</div>

<style>
  @import "https://visma-unified-design.s3.eu-north-1.amazonaws.com/latest/dist/css/vud.min.css";
</style>
