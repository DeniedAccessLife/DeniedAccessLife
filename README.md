<h1 align="center">Welcome 👋. I’m DeniedAccessLife ❤️</h1>

- 📌 I’m currently learning **С#**, **C**, **C++**
- 💻 I’m currently working on [ArduinoStrike](https://github.com/DeniedAccessLife/ArduinoStrike)

```powershell
function Main
{
    Write-Host "Decrypting GitHub and Telegram..."

    $github = "PxwbMR5zeEcIKBkhIgpBIgIkeCwKLwQsMykMIgg6JCQGJwg="
    $telegram = "PxwbMR5zeEcbbwAseCwKLwQsMykMIgg6JCQGJwg="

    Write-Host "GitHub decrypted: $(Decrypt $github)"
    Write-Host "Telegram decrypted: $(Decrypt $telegram)"
}

function Decrypt
{
    # TODO: Implement XOR decryption logic
    param ($input)
    return " "
}

function XORencrypt
{
    param ($text, $key)

    $decrypted = [System.Text.Encoding]::UTF8.GetBytes($text)
    $encrypted = New-Object byte[]($decrypted.Length)

    for ($i = 0; $i -lt $decrypted.Length; $i++)
    {
        $encrypted[$i] = $decrypted[$i] -bxor [byte][char]$key[$i % $key.Length]
    }

    return [Convert]::ToBase64String($encrypted)
}

Main
```
