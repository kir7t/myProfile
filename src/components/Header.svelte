<script>
    let menuOpen = false;

    function toggleMenu() {
        menuOpen = !menuOpen;
    }
</script>

<header class="header">
    <div class="title">
        <h1>Nekosama</h1>
    </div>

    <!-- ハンバーガーメニューのボタン -->
    <button class="menu-toggle" on:click={toggleMenu} aria-label="Toggle navigation">
        ☰
    </button>

    <nav class="nav-links {menuOpen ? 'open' : ''}">
        <a href="/about">Profile</a>
        <a href="/works">Works</a>
        <a href="/contact">Contact</a>
    </nav>
</header>

<style>
    /* ヘッダーを固定する */
    .header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 80px;
        background-color: #174a97;
        color: #ffffff;
        display: flex;
        align-items: center;
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        z-index: 1000;
        box-shadow: 0 4px 10px rgba(5, 81, 188, 0.661);
        justify-content: space-between;
        padding: 0 20px;
    }

    .title {
        font-size: 1.5rem;
    }

    /* 通常のナビゲーション */
    .nav-links {
        display: flex;
        gap: 30px;
        margin-right: 5%;
    }

    .nav-links a {
        color: #ffffff;
        text-decoration: none;
        font-size: 1rem;
    }

    .nav-links a:hover {
        color: #7cb1ff;
        text-decoration: underline;
    }

    /* ハンバーガーメニューのボタン */
    .menu-toggle {
        display: none; /* PCでは非表示 */
        background: none;
        border: none;
        font-size: 2rem;
        color: white;
        cursor: pointer;
    }

    /* =============================== */
    /* スマホ・タブレット対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .menu-toggle {
            display: block; /* スマホで表示 */
        }

        /* ナビゲーションメニューを隠す */
        .nav-links {
            display: none;
            position: absolute;
            top: 80px;
            left: 0;
            width: 100%;
            background-color: #005ce6;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            padding: 20px 0;
        }

        /* 開いたときのスタイル */
        .nav-links.open {
            display: flex;
        }

        .nav-links a {
            font-size: 1.2rem;
        }
    }
</style>
