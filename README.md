# <div align="center">Andoroid_1(μ½νλ¦°)</div>

## ππ» μ²μ νλ©΄ ππ»
### νμ€νΈλ₯Ό μλ ₯νλ EditText 2κ°μ μ°μ°μ λ²νΌ 5κ°, μ΄κΈ°ν λ²νΌμ΄ λ³΄μΈλ€.
<img alt="μ²μ νλ©΄" src="https://user-images.githubusercontent.com/102125786/184782969-5c744f13-5d28-4be0-ac52-8d888f07ba29.png">

## π± μ¬μ© λ°©λ² π±
### EditText 2κ°μ μ²«λ²μ§Έ μ«μμ λλ²μ§Έ μ«μλ₯Ό μλ ₯νκ³  μλμ μ°μ°μ λ²νΌμ λλ₯Έλ€ 

### + λ²νΌ
<img alt="μ€ννλ©΄ + " src="https://user-images.githubusercontent.com/102125786/184783501-aba83ed7-93c7-42fb-8a79-7059c08eb7c0.png">

#### - λ²νΌ
<img alt="μ€ννλ©΄ - " src="https://user-images.githubusercontent.com/102125786/184783947-be35ca4a-af60-4002-9962-8bf2024783dd.png">

#### X λ²νΌ
<img alt="μ€ννλ©΄ X " src="https://user-images.githubusercontent.com/102125786/184784289-3a3ee644-154c-4a9a-a2d0-ace80246b553.png">

#### / λ²νΌ
<img alt="μ€ννλ©΄ / " src="https://user-images.githubusercontent.com/102125786/184784386-2d12c24c-6867-490d-8b53-fd88b317e674.png">

#### % λ²νΌ
<img alt="μ€ννλ©΄ + " src="https://user-images.githubusercontent.com/102125786/184784477-3c6693d0-7bfe-4e2c-a9e5-ef43be85ee2a.png">

#### μ΄κΈ°ν λ²νΌ
<img alt="μ΄κΈ°ν" src="https://user-images.githubusercontent.com/102125786/184784769-484757bf-bf47-494f-bcf1-3d23e61c84f7.png">

#### μ«μκ° μλ λ¬Έμλ₯Ό λ£μμλ
<img alt ="μ€λ₯" src="https://user-images.githubusercontent.com/102125786/184785888-502cf5f7-1701-4b53-b7f8-a6d83b7b495f.png">

## βπ» μ€μν λ΄μ© βπ»

### findViewById
```kotlin
   private val et_number_1 : EditText by lazy{
        findViewById(R.id.et_number_1)
    }
```

### setOnClickListener
```kotlin
   btn_plus.setOnClickListener{
            setResultview(1)
        }
```
### λ²νΌ λλ₯΄λ©΄ κΈ°λ₯ κ΅¬ν 
```kotlin

   private fun setResultview(o: Int){
        try {
            val num1: Int = et_number_1.text.toString().toInt()
            val num2: Int = et_number_2.text.toString().toInt()
            var numResult : Int = -1
            when(o) {
                1 -> numResult = num1 + num2
                2 -> numResult = num1 - num2
                3 -> numResult = num1 * num2
                4 -> numResult = num1 / num2
                5 -> numResult = num1 % num2
            }
            tv_result.text = numResult.toString()
        } catch (e:Exception){
            Toast.makeText(
                this,"μ«μ μλ ₯ μ€λ₯!!",Toast.LENGTH_SHORT).show()
            }
        }

```
