<script>
    import { onMount } from 'svelte';

    import Header from '$src/components/Header.svelte';
    import Profile from '$src/components/Profile.svelte';
    import Videos from '$src/components/Videos.svelte';
    import Contact from '$src/components/Contacts.svelte';
    import Loading from '$src/components/Loading.svelte'

    let isLoading = true;

    onMount(() => {
        // 一定時間後にローディングを解除（またはデータの取得が完了したら解除）
        setTimeout(() => {
            isLoading = false;
        }, 1000); // 1秒間ローディングを表示
    });
</script>

<Loading {isLoading} />

{#if !isLoading}
    <Header />
    <main class="container mx-auto">
        <div class="mb-10 flex justify-center">
            <Profile />
        </div>
        <div class="mb-10 flex justify-center">
            <Videos />
        </div>
        <div class="mb-10 flex justify-center">
            <Contact />
        </div>
    </main>
{/if}

<style>
    main {
        margin-top: 100px;
        padding: 20px;
    }
</style>