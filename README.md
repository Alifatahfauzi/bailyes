<h1 align='center'><img alt="Baileys logo" src="https://raw.githubusercontent.com/WhiskeySockets/Baileys/refs/heads/master/Media/logo.png" height="75"/></h1>

<div align="center">

  <img src="https://files.catbox.moe/9czivv.png" />

  <a href="https://whatsapp.com/channel/0029Vb6j2u74NViqgNCLev3a">
    <img src="https://img.shields.io/badge/WhatsApp-Channel-25D366?logo=whatsapp&logoColor=white" alt="WhatsApp Channel" />
  </a>

</div>

### Custom Pairing Code

<details>
<summary style="font-weight: bold; cursor: pointer; padding: 8px; border-bottom: 1px solid #eee; margin-bottom: 5px;">Show Example</summary>
<div style="padding: 10px 15px; background: #f9f9f9; border: 1px solid #eee; border-top: none; border-radius: 0 0 5px 5px;">

```ts
if(usePairingCode && !conn.authState.creds.registered) {
    const phoneNumber = await question('Please enter your mobile phone number:\n');
    // Define your custom 8-digit code (alphanumeric)
    const customPairingCode = "BAIL-SHNY";
    const code = await conn.requestPairingCode(phoneNumber, customPairingCode);
    console.log(`Your Pairing Code: ${code?.match(/.{1,4}/g)?.join('-') || code}`);
}
```
*Note: The `question` function is a placeholder for your method of obtaining user input.*
</div>
</details>


## Install

Install in package.json:
```json
"dependencies": {
    "baileys": "github:Alifatahfauzi/bailyes"
}
```
or install in terminal:
```
npm install baileys@github:Alifatahfauzi/bailyes
```
