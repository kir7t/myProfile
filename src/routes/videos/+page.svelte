<div class="works">
    <div class="The-boy">
        <iframe 
            width="320" 
            height="180" 
            src="https://embed.nicovideo.jp/watch/sm44677799?autoplay=0"
            frameborder="0" 
            allowfullscreen>
        </iframe>
    </div>

    <div class= "Seirei">
        <iframe 
            width="320" 
            height="180" 
            src="https://embed.nicovideo.jp/watch/sm43439730?autoplay=0"
            frameborder="0" 
            allowfullscreen>
        </iframe>
    </div>
</div>

<style>
    .works {
        background-color: #a8cbff;
        border: 2px solid white;
        border-radius: 10px;
        padding: 20px;
        max-width: 900px;
        width: 90%;
        margin: auto;
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
        align-items: center;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    /* 各動画のデザイン */
    .works iframe {
        border-radius: 5px;
        border: none;
        max-width: 100%;
    }

    /* =============================== */
    /* ✅ スマホ用レスポンシブ対応 (480px以下) */
    /* =============================== */
    @media (max-width: 480px) {
        .works {
            flex-direction: column;
            gap: 15px;
        }

        .works iframe {
            width: 100%;
            height: 180px;
        }
    }

    /* =============================== */
    /* ✅ タブレット用レスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .works {
            gap: 15px;
        }

        .works iframe {
            width: 45%;
            height: 180px;
        }
    }

    /* =============================== */
    /* ✅ PC用レスポンシブ対応 (900px以上) */
    /* =============================== */
    @media (min-width: 900px) {
        .works {
            flex-wrap: nowrap;
            gap: 20px;
        }

        .works iframe {
            width: 320px;
            height: 180px;
        }
    }

</style>