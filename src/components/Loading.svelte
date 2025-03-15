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
        background-color: rgba(0, 0, 0, 0.5);
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: -1; /* 背景を後ろのレイヤーへ */
    }

    .loading-icon {
        width: 100px;
        height: 100px;
        animation: spin 1s linear infinite;
        border-radius: 50%;
    }

    .loading-script {
        position: relative;
        display: flex;
        margin-top: 510px;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #ffffff;
        font-size: 20px;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>
