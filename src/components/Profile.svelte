<script>
    //画像追加
    let images = []; // 画像を格納する配列

    function addImage() {
        // static 内の "niku.jpg" を追加
        images = [...images, "./niku.png"];
    }
</script>
<div class="container">
    <div class="profile-header">
        <h class="subject text-2xl md:text-3xl lg:text-4xl">Profile</h>
        <div class="SNS">
            <a href="https://x.com/usagidayo0" target="_blank">
                <img src="./x-logo.png" alt="X" class="x-icon w-40 h-40">
            </a>
            <a href="https://www.nicovideo.jp/user/132226324" target="_blank">
                <img src="./niconico-logo.png" alt="niconico" class="niconico-icon w-40 h-40">
            </a>
            <a href="https://youtube.com/@nekosamadayo?si=4rq6d8trqM3h9VYR" target="_blank">
                <img src="./youtube.png" alt="youtube" class="youtube-icon w-40 h-40">
            </a>
        </div>
    </div>

    <div class="profile">
        <div class="icon text-2xl md:text-3xl lg:text-4xl">
            <img 
                src="{import.meta.env.BASE_URL + 'Nekosama-icon.jpg'}" 
                alt="Nekosama" 
                class="nekosama-icon"
                on:click={addImage} 
            />
        </div>

        <div class="profile-text">
            <h class="name text-2xl md:text-3xl lg:text-4xl">Nekosama</h>
            <p class="bio text-gray-600">Composer</p>
        </div>
    </div>
    <div class="gallery">
        {#each images as imgSrc}
            <img src={imgSrc} alt="追加された画像" class="added-image">
        {/each}
    </div>
</div>

<style>
    .container {
        background-color: #a8cbff;
        border: 2px solid white;
        border-radius: 10px;
        padding: 20px;
        max-width: 900px;
        display: flex;
        flex-direction: column;  
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .profile-header {
        display: flex;
        justify-content: space-between;
    }

    .subject {
        font-weight: bold;
    }

    .name {
        font-weight: bold;
    }

    /* プロフィール欄のデザイン */
    .profile {
        display: flex;
        align-items: center;
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
        transition: transform 0.3s;
    }

    .niconico-icon {
        transition: transform 0.3s;
    }

    .youtube-icon {
        transition: transform 0.3s;
    }

    /* アイコンをホバーしたときに少し拡大 */
    .nekosama-icon:hover,
    .x-icon:hover,
    .niconico-icon:hover,
    .youtube-icon:hover {
        transform: scale(1.1);
    }

    /* =============================== */
    /* スマホ用のレスポンシブ対応 (480px以下) */
    /* =============================== */
    /* @media (max-width: 480px) {
        .container {
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


        .blank {
            margin-top: 20px;
        }
    } */

    /* =============================== */
    /* タブレット用のレスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .container {
            padding: 20px;
        }

        .subject {
            margin-top: 15px;
            margin-bottom: 15px;
            margin-left: 5px;
        }

        .profile {
            flex-direction: column;
            text-align: center;
        }

        .name {
            margin-top: 10px;
            text-align: center;
        }

        .nekosama-icon {
            width: 110px;
            height: 110px;
            margin: 0 auto;
        }

        .bio {
            text-align: center;
            margin-top: 5px;
            font-size: 16px;
        }

        .SNS {
            justify-content: center;
            gap: 15px;
        }

        .x-icon, .niconico-icon, .youtube-icon {
            width: 25px;
            height: 25px;
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
            margin-right: 20%;
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
    }
</style>