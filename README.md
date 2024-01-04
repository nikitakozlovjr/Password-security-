# Password Security

### Discription
This module helps with deep work with passwords. This module helps with password analysis, gives tips on how to improve it and offers its own solutions for improving the password.

### Password Security Analysis
___

This method is `check()` analyzes the strength of the password. The result of the function is the level of password security. It can be one of three: low, medium, high levels of reliability

```javascript
import PasswordSecurity from 'passwordSecurity';

const password1 = new PasswordSecurity('Kolayn');
const password2 = new PasswordSecurity('Kolayn2');
const password3 = new PasswordSecurity('Kolayn$2');

const security1 = password1.check(); // Low level of password security
const security2 = password2.check();// Middle level of password security
const security3 = password3.check(); // High level of password security
```

### Recommendations for increasing password security

This `boostInfo()` method gives out weak points in the password, correcting which can bring the password reliability to the maximum.

```javascript
const password1 = new PasswordSecurity('guidTv');
const password2 = new PasswordSecurity('ops');

const security1 = password1.boostInfo(); 
// The password length must be greater than 8
// The password must contain at least 1 number
// The password must contain at least 1 special character 
const security2 = password2.boostInfo(); 
// The password length must be greater than 8
// The password must contain at least 1 lowercase letter 
// The password must contain at least 1 special character 
```