<script>
    export let isLoading = true;
</script>

{#if isLoading}
    <div class="loading">
        <div class="loading-container">
            <img src="{import.meta.env.BASE_URL + 'Nekosama-icon.jpg'}" alt="Loading..." class="loading-icon">
        </div>
        <p class="loading-script">Now Loading...</p>
    </div>
{/if}

<style>
    .loading-container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh; /* 画面全体をカバー */
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 9999;
    }

    .loading-icon {
        width: 100px;
        height: 100px;
        animation: spin 1s linear infinite;
        border-radius: 50%;
    }

    .loading-script {
        display: flex;
        margin-top: 470px;
        justify-content: center;
        align-items: center;
        text-align: center;
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        color: #ffffff;
        font-size: 20px;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }

    /* @media (max-width: 480px) {
        .loading-icon{
            margin-bottom: 40px;
        }

        .loading-script {
            margin-top: 510px;
        }
    }    

    @media (max-width: 768px) {


        .loading-script {
            margin-top: 800px;
        }
    }    */
</style>
