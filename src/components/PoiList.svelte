<script>
    import {onMount, getContext} from 'svelte'
    const poiService = getContext("PoiService");


    let poiList;
    onMount(async () => {
        poiList = await poiService.getPois()
    })
</script>

<h3 class="uk-heading-divider">
    List of POIs
</h3>
<div class="uk-margin uk-width-2xlarge uk-margin-auto uk-card uk-card-default uk-card-body uk-box-shadow-large">
    <table class="uk-table">
        <thead>
        <th>Name</th>
        <th>Latitude</th>
        <th>Longitude</th>
        <th>Description</th>
        </thead>
        <tbody class="uk-text-left">
          {#if poiList}
              {#each poiList as poi}
                  <tr>
                      <td>{poi.name}</td>
                      <td>{poi.latitude}</td>
                      <td>{poi.longitude}</td>
                      <td>{poi.description}</td>
                  </tr>
              {/each}
          {/if}
        </tbody>
    </table>
</div>