# C-Sharp-ComputeHash-JS-Equivalent
Equivalent version of SHA256 ComputeHash (from C#) for JavaScript


One of the following pieces of code is written in c# and the other in javascript.
If the inputs are the same, the outputs are the same.


.Net(C#) 
```cs
  System.Security.Cryptography.SHA1 sha = new System.Security.Cryptography.SHA1CryptoServiceProvider();
            byte[] bytes = System.Text.Encoding.ASCII.GetBytes(str);
            byte[] hashingbytes = sha.ComputeHash(bytes);
            var hash = Convert.ToBase64String(hashingbytes);
            
```

JavaScript

```js
getHash = str =>{
        const hashingBytes = Buffer.from(sha1(str), "hex");
        const base64Value = Buffer.from(hashingBytes).toString('base64');
        return base64Value;
    }
```

