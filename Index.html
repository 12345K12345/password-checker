<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فحص وتوليد كلمة السر</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            text-align: center;
            padding: 40px 20px;
            color: white;
            min-height: 100vh;
            box-sizing: border-box;
        }
        .container {
            background: white;
            color: black;
            padding: 22px;
            border-radius: 14px;
            box-shadow: 0 8px 30px rgba(0,0,0,0.25);
            max-width: 420px;
            margin: auto;
        }
        h2 { margin: 0 0 12px 0; }
        .password-wrapper {
            position: relative;
            width: 100%;
        }
        input {
            padding: 12px;
            width: 100%;
            box-sizing: border-box;
            margin: 10px 0;
            border-radius: 10px;
            border: 1px solid #ccc;
            font-size: 16px;
        }
        .toggle-btn {
            position: absolute;
            top: 50%;
            right: 10px;
            transform: translateY(-50%);
            background: none;
            border: none;
            cursor: pointer;
            font-size: 14px;
            color: #2575fc;
        }
        .buttons {
            display: flex;
            gap: 8px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 8px;
        }
        button {
            padding: 10px 14px;
            border: none;
            background: #2575fc;
            color: white;
            border-radius: 10px;
            cursor: pointer;
            font-size: 14px;
        }
        button:hover { opacity: 0.95; }
        .strength {
            font-size: 16px;
            margin-top: 12px;
            font-weight: bold;
            min-height: 22px;
        }
        .meter {
            height: 10px;
            background: #eee;
            border-radius: 8px;
            overflow: hidden;
            margin-top: 10px;
        }
        .meter-fill {
            height: 100%;
            width: 0%;
            transition: width .25s ease, background-color .25s ease;
        }
        .suggestions {
            font-size: 13px;
            color: #555;
            margin-top: 8px;
            min-height: 18px;
        }
        footer {
            margin-top: 20px;
            font-size: 14px;
            color: #888;
        }
        @media (max-width: 480px) {
            .container { padding: 18px; }
            button { width: 48%; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>🔒 فحص وتوليد كلمة السر</h2>

        <div class="password-wrapper">
            <input type="password" id="password" placeholder="أدخل كلمة السر" oninput="checkPassword()">
            <button type="button" class="toggle-btn" onclick="togglePassword()">👁</button>
        </div>

        <div class="buttons">
            <button onclick="generatePassword(12)">توليد كلمة سر قوية 🔑</button>
            <button id="copyBtn" onclick="copyPassword()">نسخ</button>
        </div>

        <div class="strength" id="result"></div>
        <div class="meter" aria-hidden="true"><div id="meterFill" class="meter-fill"></div></div>
        <p id="suggestions" class="suggestions"></p>

        <footer>
            تم التطوير بواسطة: <strong>Kerolos Mansy</strong>
        </footer>
    </div>

    <script>
        function checkPassword() {
            const password = document.getElementById('password').value;
            let score = 0;

            if (password.length >= 8) score++;
            if (/[A-Z]/.test(password)) score++;
            if (/[a-z]/.test(password)) score++;
            if (/[0-9]/.test(password)) score++;
            if (/[^A-Za-z0-9]/.test(password)) score++;

            const result = document.getElementById('result');
            const meterFill = document.getElementById('meterFill');
            const suggestionsEl = document.getElementById('suggestions');

            if (password.length === 0) {
                result.textContent = '';
                meterFill.style.width = '0%';
                suggestionsEl.textContent = '';
                return;
            }

            if (score <= 2) {
                result.textContent = '❌ كلمة السر ضعيفة';
                meterFill.style.backgroundColor = '#e74c3c';
            } else if (score === 3) {
                result.textContent = '⚠️ كلمة السر متوسطة';
                meterFill.style.backgroundColor = '#f39c12';
            } else {
                result.textContent = '✅ كلمة السر قوية';
                meterFill.style.backgroundColor = '#2ecc71';
            }

            meterFill.style.width = (score / 5 * 100) + '%';

            const suggestions = [];
            if (password.length < 8) suggestions.push('زوّد الطول (8 أحرف أو أكثر)');
            if (!/[A-Z]/.test(password)) suggestions.push('ضع حرف كبير');
            if (!/[a-z]/.test(password)) suggestions.push('ضع حرف صغير');
            if (!/[0-9]/.test(password)) suggestions.push('أضف رقم');
            if (!/[^A-Za-z0-9]/.test(password)) suggestions.push('أضف رمز خاص');

            suggestionsEl.textContent = suggestions.join(' • ');
        }

        function generatePassword(length = 12) {
            const upper = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
            const lower = 'abcdefghijklmnopqrstuvwxyz';
            const digits = '0123456789';
            const symbols = '!@#$%^&*()_+~`|}{[]:;?><,./-=';
            let pwd = '';
            pwd += upper.charAt(Math.floor(Math.random() * upper.length));
            pwd += lower.charAt(Math.floor(Math.random() * lower.length));
            pwd += digits.charAt(Math.floor(Math.random() * digits.length));
            pwd += symbols.charAt(Math.floor(Math.random() * symbols.length));
            const all = upper + lower + digits + symbols;
            for (let i = 4; i < length; i++) {
                pwd += all.charAt(Math.floor(Math.random() * all.length));
            }
            pwd = pwd.split('').sort(() => 0.5 - Math.random()).join('');
            document.getElementById('password').value = pwd;
            checkPassword();
        }

        function copyPassword() {
            const pwd = document.getElementById('password').value;
            if (!pwd) {
                alert('ما في كلمة لنسخها!');
                return;
            }
            navigator.clipboard.writeText(pwd).then(() => {
                const b = document.getElementById('copyBtn');
                const old = b.textContent;
                b.textContent = 'تم النسخ ✓';
                setTimeout(() => b.textContent = old, 1400);
            }).catch(() => {
                alert('فشل النسخ — جرب نسخه يدويًا.');
            });
        }

        function togglePassword() {
            const pwdField = document.getElementById('password');
            const btn = event.target;
            if (pwdField.type === 'password') {
                pwdField.type = 'text';
                btn.textContent = '🙈';
            } else {
                pwdField.type = 'password';
                btn.textContent = '👁';
            }
        }
    </script>
</body>
</html>
