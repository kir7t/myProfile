<div class="container">
    <div class="contacts">
        <h class="subject text-xl md:text-2xl lg:text-3xl" id="contacts-section">Contact</h>
        <p class="mail-adress text-center">nekosamadayoo0@gmail.com</p>
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

    /* Gmailタイトル */
    .subject {
        font-size: 24px;
        font-weight: bold;
        margin-top: 5px;
        margin-bottom: 10px;
    }

    /* メールアドレス */
    .mail-adress {
        word-break: break-all; /* メールアドレスが枠からはみ出さないように */
        color: #333;
    }

    /* =============================== */
    /* ✅ スマホ用レスポンシブ対応 (480px以下) */
    /* =============================== */
    @media (max-width: 480px) {
        .contacts {
            padding: 15px;
        }

        .subject {
            font-size: 20px;
            margin-top: 5px;
        }

        .mail-adress {
            font-size: 2px;
        }
    }

    /* =============================== */
    /* ✅ タブレット用レスポンシブ対応 (768px以下) */
    /* =============================== */
    @media (max-width: 768px) {
        .subject {
            font-size: 25px;
            margin-top: 10px;
            margin-left: 10px;
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

        .subject {
            font-size: 30px;
            margin-top: 15px;
            margin-left: 10px;
        }

        .mail-adress {
            font-size: 18px;
        }
    }
</style>