<div class="container">
    <h class="subject text-xl md:text-2xl lg:text-3xl" id="works-section">Works</h>
    <div class="works">
        <div class="the-boy">
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
        justify-content: center;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .subject {
        font-weight: bold;
        margin-top: 10px;
    }

    .works {
        justify-content: center;
        align-items: center;
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
    /* @media (max-width: 480px) {
        .works {
            display: flex;
            flex-direction: column;
            justify-content: center; 
            align-items: center; 
            gap: 15px;
        }

        .subject {
            margin-top: 5px;
            margin-bottom: 10px;
        }

        .works iframe {
            width: 100%;
            height: 180px;
        }
    } */

    /* =============================== */
    /* ✅ タブレット用レスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .works {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .subject {
            margin-top: 10px;
            margin-bottom: 20px;
            margin-left: 5px;
        }
    }

    /* =============================== */
    /* ✅ PC用レスポンシブ対応 (900px以上) */
    /* =============================== */
    @media (min-width: 900px) {
        .works {
            display: flex;
            gap: 40px;
        }

        .subject {
            font-size: 30px;
            margin-top: 15px;
            padding-bottom: 30px;
            margin-left: 10px;
        }
    }
</style>