<div class="contacts">
    <h class="gmail text-3xl text-gray-600">Gmail</h>
    <p class="mail-adress text-2xl text-gray-600">nekosamadayo@gmail.com</p>
</div>

<style>
    .contacts {
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
        font-family: "Press Start 2P", DotGothic16, sans-serif;
        text-align: center;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    /* Gmailタイトル */
    .gmail {
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 10px;
    }

    /* メールアドレス */
    .mail-adress {
        font-size: 18px;
        word-break: break-all; /* メールアドレスが枠からはみ出さないように */
        color: #333;
    }

    /* =============================== */
    /* ✅ スマホ用レスポンシブ対応 (480px以下) */
    /* =============================== */
    @media (max-width: 480px) {
        .contacts {
            width: 95%;
            padding: 15px;
        }

        .gmail {
            font-size: 18px;
        }

        .mail-adress {
            font-size: 14px;
        }
    }

    /* =============================== */
    /* ✅ タブレット用レスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .contacts {
            width: 90%;
        }

        .gmail {
            font-size: 20px;
        }

        .mail-adress {
            font-size: 16px;
        }
    }

    /* =============================== */
    /* ✅ PC用レスポンシブ対応 (900px以上) */
    /* =============================== */
    @media (min-width: 900px) {
        .contacts {
            max-width: 900px;
        }

        .gmail {
            font-size: 24px;
        }

        .mail-adress {
            font-size: 18px;
        }
    }


</style>