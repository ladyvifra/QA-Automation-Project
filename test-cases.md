# Test Cases for Login Page

## TC_001: Validar inicio de sesión exitoso

**Precondiciones:**
- La página de inicio de sesión debe estar cargada.

**Pasos de prueba:**
1. Ingresar el nombre de usuario `tomsmith`.
2. Ingresar la contraseña `SuperSecretPassword!`.
3. Hacer clic en el botón "Login".

**Datos de prueba:**
- Usuario: `tomsmith`
- Contraseña: `SuperSecretPassword!`

**Resultado esperado:**
- Redirigir a una página principal que muestra el mensaje: "You logged into a secure area!"

---

## TC_002: Validar mensaje de error para credenciales incorrectas

**Precondiciones:**
- La página de inicio de sesión debe estar cargada.

**Pasos de prueba:**
1. Ingresar el nombre de usuario `usuarioInvalido`.
2. Ingresar la contraseña `password123`.
3. Hacer clic en el botón "Login".

**Datos de prueba:**
- Usuario: `usuarioInvalido`
- Contraseña: `password123`

**Resultado esperado:**
- Mostrar un mensaje de error en la parte superior: "Your username is invalid!"

---

## TC_003: Validar campos obligatorios

**Precondiciones:**
- La página de inicio de sesión debe estar cargada.

**Pasos de prueba:**
1. Dejar el campo de nombre de usuario vacío.
2. Ingresar la contraseña `SuperSecretPassword!`.
3. Hacer clic en el botón "Login".

**Resultado esperado:**
- Mostrar un mensaje de error indicando que el nombre de usuario es obligatorio.
- El sistema no debe permitir iniciar sesión.

---

## TC_004: Validar que el campo de contraseña sea obligatorio

**Precondiciones:**
- La página de inicio de sesión debe estar cargada.

**Pasos de prueba:**
1. Ingresar el nombre de usuario `tomsmith`.
2. Dejar el campo de contraseña vacío.
3. Hacer clic en el botón "Login".

**Resultado esperado:**
- Mostrar un mensaje de error indicando que la contraseña es obligatoria.
- El sistema no debe permitir iniciar sesión.

---

## TC_005: Validar límite de caracteres en los campos

**Precondiciones:**
- La página de inicio de sesión debe estar cargada.

**Pasos de prueba:**
1. Ingresar un nombre de usuario con más de 50 caracteres.
2. Ingresar una contraseña con más de 50 caracteres.
3. Hacer clic en el botón "Login".

**Datos de prueba:**
- Usuario: `usuarioConTextoMuyLargoNoValido123456789012345678901234567890`
- Contraseña: `passwordConTextoMuyLargoNoValido123456789012345678901234567890`

**Resultado esperado:**
- El sistema debe restringir la longitud máxima de entrada a 50 caracteres.
- Mostrar un mensaje de error si el límite es excedido.

---

## TC_006: Validar ingreso de caracteres especiales en el nombre de usuario

**Precondiciones**
- La página de inicio de sesión debe estar cargada

** Pasos de prueba**
1. Ingresar un nombre de usuario con caracteres especiales, por ejemplo, tom@smith!
2. Ingresar una contraseña válida, por ejemplo, SuperSecretPassword
3. Hacer clic en el botón "Login".

**Datos de prueba**
- Usuario: tom@smith!
- Contraseña: SuperSecretPassword!

**Resultado esperado**
- El sistema debe aceptar el nombre de usuario si los caracteres especiales son válidos o debe mostrar un mensaje de error si no lo son.
