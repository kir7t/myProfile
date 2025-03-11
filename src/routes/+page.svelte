<script>
    import Header from '$src/components/Header.svelte';
    import Videos from '$src/routes/videos/+page.svelte';
    import Contact from '$src/routes/contacts/+page.svelte';
</script>

<Header />
<main>
</main>

<div class="container">
    <div class="profile">
        <div class="icon">
            <img src="/Nekosama-icon.jpg" alt="Nekosama" class="Nekosama-icon">
        </div>
        <p class="bio text-2xl text-gray-600">Garagebandを用いて曲を作ります</p>
    </div>

    <div class="SNS">
        <a href="https://x.com/usagidayo0" target="_blank">
            <img src="/x-logo.png" alt="X" class="x-icon">
        </a>
        <a href="https://www.nicovideo.jp/user/132226324" target="_blank">
            <img src="/niconico-logo.png" alt="NicoNico" class="niconico-icon">
        </a>
    </div>
</div>

<Videos />
<Contact />

<style>
    .container {
        background-color: #a8cbff;
        border: 2px solid white;
        border-radius: 10px;
        padding: 20px;
        max-width: 900px;
        width: 90%;
        margin: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    /* プロフィール欄のデザイン */
    .profile {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    /* アイコンのデザイン */
    .Nekosama-icon {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        margin-left: 30%;
        object-fit: cover;
    }

    /* Bio文のデザイン */
    .bio {
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        margin-right: 5%;
        text-align: right;
        font-size: 18px;
    }

    /* SNSアイコンのデザイン */
    .SNS {
        display: flex;
        gap: 20px;
        margin-top: 20px;
    }

    .x-icon {
        width: 40px;
        height: 40px;
        transition: transform 0.3s;
    }

    .niconico-icon {
        width: 80px;
        height: 80px;
        transition: transform 0.3s;
    }

    /* アイコンをホバーしたときに少し拡大 */
    .x-icon:hover,
    .niconico-icon:hover {
        transform: scale(1.1);
    }

    /* =============================== */
    /* スマホ用のレスポンシブ対応 (480px以下) */
    /* =============================== */
    @media (max-width: 480px) {
        .container {
            width: 90%;
            padding: 15px;
        }

        .profile {
            flex-direction: column;
            text-align: center;
        }

        .Nekosama-icon {
            width: 100px;
            height: 100px;
            margin: 0 auto;
        }

        .bio {
            margin-top: 10px;
            text-align: center;
            font-size: 14px;
        }

        .SNS {
            flex-direction: column;
            gap: 10px;
        }

        .x-icon, .niconico-icon {
            width: 35px;
            height: 35px;
        }
    }

    /* =============================== */
    /* タブレット用のレスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .container {
            width: 85%;
            padding: 20px;
        }

        .profile {
            flex-direction: column;
            text-align: center;
        }

        .Nekosama-icon {
            width: 110px;
            height: 110px;
            margin: 0 auto;
        }

        .bio {
            text-align: center;
            margin-top: 15px;
            font-size: 16px;
        }

        .SNS {
            justify-content: center;
            gap: 15px;
        }

        .x-icon, .niconico-icon {
            width: 40px;
            height: 40px;
        }
    }

    /* =============================== */
    /* ✅ PC用のレスポンシブ対応 (900px以上) */
    /* =============================== */
    @media (min-width: 900px) {
        .container {
            max-width: 900px;
        }

        .profile {
            flex-direction: row;
            justify-content: space-between;
        }

        .Nekosama-icon {
            width: 200px;
            height: 200px;
        }

        .bio {
            text-align: right;
            font-size: 18px;
        }

        .SNS {
            gap: 20px;
        }

        .x-icon, .niconico-icon {
            width: 45px;
            height: 45px;
        }
    }

    /* =============================== */
    /* ✅ 共通設定 */
    /* =============================== */
    main {
        margin-top: 100px;
        padding: 20px;
    }

    p {
        margin-bottom: 20px;
    }

</style>