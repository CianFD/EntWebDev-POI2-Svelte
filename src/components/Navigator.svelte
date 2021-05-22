<script>
    import Title from "./Title.svelte";
    export let navBar;
</script>

<div class="uk-flex uk-flex-center uk-flex-middle uk-text-center uk-grid-small" uk-grid>
    <Title title="Donations" subTitle="Select Donations or Candidates" />
    <div>
        <ul class="uk-iconnav uk-margin-left uk-margin-right">
            {#each navBar as nav}
                <a href="{nav.link}" class="uk-card uk-card-small uk-card-hover uk-padding-small">
                    <i class="{nav.icon}" style="{nav.colour}" uk-tooltip="title: {nav.title}; pos:bottom"></i>
                </a>
            {/each}
        </ul>
    </div>
</div>