# Materi Tanggal 27-1 Juli

---

## 1.React JS

React JS adalah library JavaScript yang biasa digunakan saat membangun UI (User Interface) suatu website atau aplikasi web.

~ Instalasi React JS
Step 1. Instal node js
Step 2. Use library create-react-app

```
catatan
- npx create-react-app my-app
- npm create-react-app-(dengan nama file) => membuat sebuah react baru
- npm run start
- npm start => menjalankan react
```

contoh

```js
(Hello.jsx)
function Hello() {
    return (
        <div>
        <p>HELLO</p>
        </div>
    );
};

export default hello;

(App.js)
import {Hello} from "./Hello"
function App() {
    return (
        // memanggil function hello
        <Hello />
    );
};
export default App;
```

```notes
Sekali membuat sebuah fungsi di react bisa digunakan berkali kali.
```

####JSX
jsx dikenal juga dengan javascrip xml. Dengan jsx kita dapat menggunkan HTML di dalam file extension javascrip.
setiap JSX hanya dapat menggunakan 1 parent element

```js
contoh
return(
    <p>Hello<p>
)
//// ini salah
return(
    <p>Hello</p>
    <p>World</p>
)
///kalau mau harus menggunakan tag element <div> atau element kosong <>
return(
    <div> atau <>
    <p>Hello</p>
    <p>World</p>
    <div/> atau </>
)
```

####Virtual DOM
Dengan DOM dapat berinteraksi seperti mengupdate data pada web. React js mempunyai fitur Virtual DOM yang mengupdate data tanpa perlu ngerefresh halaman.

####Class
Didalam jsx tidak boleh menggunakan attribut class harus menggunkan className

####Curly Braces
kita bisa menggunakan syntax javascrip didalam element html dengan curly breces
curly braces bisa akses variabel pada jsx

`````js
contoh
function Hello() {
 /// deklarasi variabel
 const name = ' Lala '
 return(
    <div>
///// memanggil variabel
    <p>name</p>
    </div>
 )
}
#### conditional in jsx
membuat conditional didalam react bisa menggunakan conditional ternary operator
````js
contoh
function Hello() {
    const Login = true
 return(
    ///conditional ternary
    {Login ? <p>sudah masuk<p> : <p>belum masuk<p>}
 )
}
#### Looping di react
looping di react bisa mrnggunakan maping
````js
contoh
function Hello() {
    const data = [
        {buah: "mangga"}, {buah: "jeruk"}
    ]}
return(
///maping menampilkan array of object
    {data.map((item, index)=> (
     <p key={index}>{item.buah}</p>
    ))
    }
)
````

# 2 Component
component adalah salah satu code dari react js
componen membagi UI dalam satuan satuan kecil. yang artinya dalam 1 page ada beberapa component yang bisa di buat.

- membuat component
terdapat 2 cara
1 gunakan function
2 gunakan class

#3 State
State adalah data yang di miliki oleh sebuah komponen (statefull component)
dan ada kemungkinan data dapat di ubah.
membuat state di react membutuhkan useState()
````js
contoh
const [nama,setNama] = useState("lala");
````
cara penggunaan useState
````js
/// 1 import useState dari react
import { useState } from "react";
////2 menulis useState
const [nama,setNama] = useState("lala");
///3 pengambilan data
<p> halo,saya { nama } </p>
`````

# 4 useEffect

useEffect merupakan hooks yang bisa di gunakan untuk menggunakan lifecycle pada funcitonal dengan mudah.

cara penggunaan useEffect

```js
contoh
1 import useEffect
import { useEffect } from "react"
2 tulis penggunana useEffect
function Hello() {
 const name = ' Lala '
 useEffect (() => {
    console.log()}, [name]
 })
 return(
    <div>
```
