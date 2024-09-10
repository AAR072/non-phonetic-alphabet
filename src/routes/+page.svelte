  
<script>
import "carbon-components-svelte/css/g100.css";
import { TextInput } from "carbon-components-svelte";
  import {
    Header,
    HeaderNav,
    HeaderNavItem,
    HeaderNavMenu,
    SkipToContent,
    Content,
    Grid,
    Row,
    Column,
  } from "carbon-components-svelte";

  let isSideNavOpen = false;
  let inputText = ""
</script>

<Header company="IBM" platformName="Carbon Svelte" bind:isSideNavOpen>
  <svelte:fragment slot="skip-to-content">
    <SkipToContent />
  </svelte:fragment>
  <HeaderNav>
    <HeaderNavItem href="/" text="Link 1" />
    <HeaderNavItem href="/" text="Link 2" />
    <HeaderNavItem href="/" text="Link 3" />
    <HeaderNavMenu text="Menu">
      <HeaderNavItem href="/" text="Link 1" />
      <HeaderNavItem href="/" text="Link 2" />
      <HeaderNavItem href="/" text="Link 3" />
    </HeaderNavMenu>
  </HeaderNav>
</Header>

<Content>
  <Grid>
    <Row>
      <Column>
      <h1>Troll Scammers</h1>
      <br>
      <h2>Try now<h2>
      <br>
      <TextInput size="xl" 
      bind:value={inputText}
       on:keyup={() => alert(name)} placeholder="John Doe"/>
      <br>
      <h2>Or see some examples<h2>
      </Column>
    </Row>
  </Grid>
</Content>

