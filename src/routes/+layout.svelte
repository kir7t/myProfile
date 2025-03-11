<script>
	// import { Header } from "$components/Header.svelte";
</script>
  
<slot />

<style>
    :global(body) {
        background-color: #437ed8; /* 好きな色に変更 */
        margin: 0;
        padding: 0;
        min-height: 100vh; /* 高さを画面いっぱいにする */
    }
</style>

