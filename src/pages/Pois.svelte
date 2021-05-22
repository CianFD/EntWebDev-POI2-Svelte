<script>
    import PoiList from "../components/PoiList.svelte";
    import report from "/src/assets/report.png";
</script>

<div class="uk-text-center" uk-grid>
    <div class="uk-width-2-5@m ">
        <img width="300" src="{report}" alt="report">
    </div>
    <div class="uk-width-3-5@m ">
        <div class="uk-card uk-card-default uk-card-body uk-box-shadow-large uk-width-2xlarge ">
            <PoiList/>
        </div>
    </div>
</div>