<script>
  import { setContext } from "svelte";
  import Pois from "./pages/Pois.svelte"
  import {PoiService} from "./services/poi-service";
  import Users from "./pages/Users.svelte";
  import Navigator from "./components/Navigator.svelte";
  import Router from "svelte-spa-router";

  setContext("PoiService", new PoiService("http://localhost:4000"));

  let routes = {
    "/candidates": Candidates,
    "/donations": Donations,
  }

  const navBar = [{
    title: "Donations",
    icon: "fas fa-hand-holding-usd fa-3x",
    colour: "color:rgb(153, 196, 74)",
    link: "/#/donations",
  }, {
    title: "Candidates",
    icon: "fas fa-clipboard-list fa-3x",
    colour: "color:rgb(63, 122, 139)",
    link: "/#/candidates",
  }];

</script>

<div class="uk-container">
  <Navigator {navBar}/>
  <Router {routes} />
</div>