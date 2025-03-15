<script>
    let menuOpen = false;

    function toggleMenu() {
        menuOpen = !menuOpen;
    }
</script>

<header class="header">
    <div class="title text-3xl md:text-4xl lg:text-5xl  flex justify-center items-center">
        <h1>Nekosama</h1>
    </div>

    <!-- ハンバーガーメニューのボタン -->
    <span class="menu-toggle text-6xl flex justify-center items-center relative bottom-1" on:click={toggleMenu} aria-label="Toggle navigation">
        ☰
    </span>

    <nav class="nav-links {menuOpen ? 'open' : ''} md:text-lg lg:text-2xl flex justify-center items-center">
        <a href="#">Profile</a>
        <a href="#works-section">Works</a>
        <a href="#contacts-section">Contact</a>
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
        z-index: 1000;
        box-shadow: 0 4px 10px rgba(5, 81, 188, 0.661);
        justify-content: space-between;
        padding: 0 20px;
    }

    /* 通常のナビゲーション */
    .nav-links {
        display: flex;
        gap: 20px;
    }

    .nav-links a {
        color: #ffffff;
        text-decoration: none;
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
