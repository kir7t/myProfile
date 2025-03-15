<script>
    import Header from '$src/components/Header.svelte';
    import Videos from '$src/routes/videos/+page.svelte';
    import Contact from '$src/routes/contacts/+page.svelte';

    //Loading
    import Loading from '$src/components/Loading.svelte'
    import { onMount } from 'svelte';

    let isLoading = true;

    onMount(() => {
        // 一定時間後にローディングを解除（またはデータの取得が完了したら解除）
        setTimeout(() => {
            isLoading = false;
        }, 1000); // 2秒間ローディングを表示
    });

    //画像追加
    let images = []; // 画像を格納する配列

    function addImage() {
        // static 内の "niku.jpg" を追加
        images = [...images, "./niku.png"];
    }
    //
</script>

<Loading {isLoading} />

{#if !isLoading}
    <Header />
    <main>
        <div class="container">
            <div class="profile-header">
                <h class="subject" >Profile</h>
                <div class="SNS">
                    <a href="https://x.com/usagidayo0" target="_blank">
                        <img src="./x-logo.png" alt="X" class="x-icon">
                    </a>
                    <a href="https://www.nicovideo.jp/user/132226324" target="_blank">
                        <img src="./niconico-logo.png" alt="niconico" class="niconico-icon">
                    </a>
                    <a href="https://youtube.com/@nekosamadayo?si=4rq6d8trqM3h9VYR" target="_blank">
                        <img src="./youtube.png" alt="youtube" class="youtube-icon">
                    </a>
                </div>
            </div>

            <div class="profile">
                <div class="icon">
                    <img 
                        src="{import.meta.env.BASE_URL + 'Nekosama-icon.jpg'}" 
                        alt="Nekosama" 
                        class="nekosama-icon"
                        on:click={addImage} 
                    />
                </div>

                <div class="profile-text">
                    <h class="name">Nekosama</h>
                    <p class="bio text-gray-600">Composer</p>
                </div>


                
            </div>
            <div class="gallery">
                {#each images as imgSrc}
                    <img src={imgSrc} alt="追加された画像" class="added-image">
                {/each}
            </div>
        </div>

        <div class="blank">
        </div>
        <Videos />
        <div class="blank">
        </div>
        <Contact />
        <div class="blank">
        </div>
    </main>
{/if}

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
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .profile-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .subject {
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        font-weight: bold;
        font-size: 18px;
        margin-top: 10px;
    }

    /* スムーズスクロールを適用 */
    html {
        scroll-behavior: smooth;
    }

    .name {
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        font-weight: bold;
        margin-top: 10px;
        display: block;
    }

    /* プロフィール欄のデザイン */
    .profile {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .profile-text {
        display: flex;
        flex-direction: column; /* 縦並び */
    }

    .gallery {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-top: 20px;
        justify-content: center;
    }

    .added-image {
        width: 30px;
        height: 30px;
        object-fit: cover;
        border-radius: 10px;
    }

    /* アイコンのデザイン */
    .nekosama-icon {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        margin-left: 80%;
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
        gap: 20px;
        margin-top: 20px;
        display: flex;
        justify-content: center;
        align-items: left;
    }

    .x-icon {
        width: 40px;
        height: 40px;
        transition: transform 0.3s;
    }

    .niconico-icon {
        width: 40px;
        height: 40px;
        transition: transform 0.3s;
    }

    .youtube-icon {
        width: 40px;
        height: 40px;
        transition: transform 0.3s;
    }

    /* アイコンをホバーしたときに少し拡大 */
    .nekosama-icon:hover,
    .x-icon:hover,
    .niconico-icon:hover,
    .youtube-icon:hover {
        transform: scale(1.1);
    }

    .blank {
        margin-top: 10px;
    }

    /* =============================== */
    /* スマホ用のレスポンシブ対応 (480px以下) */
    /* =============================== */
    @media (max-width: 480px) {
        .container {
            max-width: 80%;
            padding: 15px;
        }

        .subject {
            font-size: 30px;
            margin-bottom: 10px;
        }

        .profile {
            flex-direction: column;
            text-align: center;
        }

        .profile-text {
            text-align: center;
        }

        .name {
            font-size: 20px;
        }

        .nekosama-icon {
            width: 100px;
            height: 100px;
            margin: 0 auto;
        }

        .bio {
            margin-top: 10px;
            text-align: center;
            font-size: 15px;
        }

        .SNS {
            display: flex;
            gap: 10px;
        }

        .x-icon, .niconico-icon, .youtube-icon {
            width: 10px;
            height: 10px;
        }

        .blank {
            margin-top: 20px;
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

        .subject {
            font-size: 30px;
            margin-top: 15px;
            margin-bottom: 15px;
            margin-left: 10px;
        }

        .profile {
            flex-direction: column;
            text-align: center;
        }

        .profile-text {
            align-items: flex-start;
            margin-right: 60px;
        }

        .name {
            font-size: 25px;
        }

        .nekosama-icon {
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

        .x-icon, .niconico-icon, .youtube-icon {
            width: 40px;
            height: 40px;
        }

        .blank {
            margin-top: 30px;
        }
    }

    /* =============================== */
    /* ✅ PC用のレスポンシブ対応 (900px以上) */
    /* =============================== */
    @media (min-width: 900px) {
        .container {
            max-width: 900px;
        }

        .subject {
            font-size: 30px;
            margin-top: 20px;
            margin-bottom: 20px;
            margin-left: 10px;
        }

        .profile {
            margin-top: 20px;
            margin-bottom: 20px;
            flex-direction: row;
            justify-content: space-between;
        }

        .profile-text {
            align-items: flex-start;
            margin-right: 25%;
        }

        .name {
            font-size: 30px;
        }

        .nekosama-icon {
            width: 200px;
            height: 200px;
        }

        .bio {
            text-align: right;
            font-size: 18px;
        }

        .SNS {
            gap: 20px;
            margin-right: 15px;
        }

        .x-icon, .niconico-icon, .youtube-icon {
            width: 40px;
            height: 40px;
        }

        .blank {
            margin-top: 40px;
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