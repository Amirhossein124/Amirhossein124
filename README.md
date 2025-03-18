- 👋 Hi, I’m @Amirhossein124
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Amirhossein124/Amirhossein124 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>جستجوی کاربر</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            direction: rtl;
        }
        input, button {
            padding: 10px;
            margin: 10px;
        }
        #result {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>جستجوی کاربر</h1>
    <input type="text" id="userCode" placeholder="کد کاربر را وارد کنید">
    <button onclick="searchUser()">جستجو</button>
    <div id="result"></div>

    <script>
        // اطلاعات کاربران
        const users = [
            { code: '001', name: 'علی', score: 95 },
            { code: '002', name: 'رضا', score: 88 },
            { code: '003', name: 'سارا', score: 92 }
        ];

        // تابع جستجوی کاربر
        function searchUser() {
            const userCode = document.getElementById('userCode').value;
            const resultDiv = document.getElementById('result');
            const user = users.find(u => u.code === userCode);

            if (user) {
                resultDiv.innerHTML = `نام: ${user.name}, امتیاز: ${user.score}`;
            } else {
                resultDiv.innerHTML = 'کاربر یافت نشد.';
            }
        }
    </script>
</body>
</html>
