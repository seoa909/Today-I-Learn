# 이메일 함수

- 해당 코드는 타입을 전혀 모르겠어서 그냥 any로 해버린 anyScript입니다.
- 그 외에 코드들은 nodemailer 프레임워크에 맞게 따라 한거니, 외울필요도 없음
```js
const nodemailer = require("nodemailer");
module.exports = async (email: any, subject: any, text: any) => {
    try {
        const transporter = nodemailer.createTransport({
            host: process.env.HOST,
            service: process.env.SERVICE,
            port: 465,
            secure: true,
            auth: {
                user: process.env.USER,
                pass: process.env.PASS
            }
        });

        await transporter.sendMail({
            from: process.env.USER,
            to: email,
            subject: subject,
            text: text
        });
    } catch (error) {
        console.log(error);
    }
};

```
