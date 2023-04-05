# Aprendendo Lua
### Um guia básico sobre a linguagem de programação Lua

<div style="display:flex;">
     <img src="https://img.shields.io/badge/-Lua-2C2D72?logo=Lua&logoColor=white" width="60px">
</div>

---

## 🌑 Onde baixar Lua?
### [𝙎𝙞𝙩𝙚 𝙊𝙛𝙞𝙘𝙞𝙖𝙡](https://www.lua.org/download.html)

---

## 🌒 LuaRocks - gerenciador de pacotes Lua 
### [𝙎𝙞𝙩𝙚 𝙊𝙛𝙞𝙘𝙞𝙖𝙡](https://luarocks.org)

---

## 🌓 Aprendendo o Básico

### ✱ Comentando em Lua:
```
-- 
print("Olá Mundo") -- 

--[[
  Comentário 
  Com multilinhas
]]
```
#### ✱ Usamos ```--``` para criar comentários.
#### ✱ Usamos ```--[[ ]]``` para criar comentários com multilinhas.

---

### ✱ Print com Lua:
```
print("Printando em Lua!")
```
#### ✱ O print de Lua é semelhante ao de Python ```print("")```
#### ✱ Usar vírgula ```print("Olá mundo", Algo_aqui)``` servirá como "TAB".
#### ✱ Usar ponto ponto ```print("Olá mundo" .. Algo_aqui)``` servirá como "+" no Python (Serve para concatenação).

---

### ✱ Variáveis:
```
-- TIPOS
local x = 100 -- Números 
local linguagem = "Lua" -- String
local melhor_linguagem = true -- Boolean
local a = nil -- Sem valor ou valor inválido

-- Incremento em números
local n = 1
n = n + 1
print(n) -- 2

-- Strings
-- Concatenar strings
local linguagem = "Lua"
local qualidade = "é incrível"

print(linguagem .. " " .. qualidade) -- Lua é incrível
print("Lua " .. "é incrível)
```

---

### ✱ Operadores de comparação:
```
  == Igualdade
  <  Menos que
  >  Maior que
  <= Menor ou igual a
  >= Maior ou igual a
  ~= Desigualdade
```

---

### ✱ Declarando condicionais:
```
-- Comparação de números
local idade = 20

if idade > 18 then
  print("Mais de 18") 
end

-- elseif e else
idade = 20

if idade > 18 then
  print("Mais de 18")
elseif idade == 18 then
  print("Tem 18")
else
  print("De menor!")
end

-- Comparação de boolean
local forte = true

if forte then
    print(É um monstro!")
end

-- Comparações de strings
local linguagem = "Lua"

if name ~= "Lua" then
  print("Não é Lua!")
end
```

---

### ✱ Funções:
```
-- Usando a palavra-chave function
local function print_num(a)
  print(a)
end

-- Usando uma expressão de função anônima
local print_num = function(a)
  print(a)
end

-- Chamando a função com o argumento 5
print_num(5) -- Imprime 5

-- Vários parâmetros
function sum(a, b)
  return a + b
end
```

---

### ✱ Loops:
#### While
```
local i = 1

while i <= 3 do
   print("Olá")
   i = i + 1
end
```
#### For
```
for i = 1, 3 do
   print("Olá")
end
```
#### ✱ Ambos imprimem "Olá" 3 vezes

---

### ✱ Tabelas:
```
 -- As tabelas podem ser usadas para armazenar dados complexos.
 -- Tipos de tabelas: arrays (listas) e dicts (chave, valor)
```
#### Arrays
```
local cores = { "Azul", "Verde", "Vermelho" }

print(cores[1]) -- Azul

-- Diferentes maneiras de percorrer listas
-- #cores é o comprimento da tabela

for i = 1, #cores do
  print(cores[i])
end

-- ipairs 
for index, value in ipairs(cores) do
   print(cores[index])
   -- or
   print(value)
end

-- Se você não usar índice ou valor aqui, poderá substituí-lo por "_"
for _, value in ipairs(cores) do
   print(value)
end
```
#### Dicionários
```
local info = { 
   nome = "Lua",
   idade = 30,
   usual = true
}

-- Ambos imprimem Lua
print(info["nome"])
print(info.nome)

-- Loop por pares
for key, value in pairs(info) do
   print(key .. " " .. tostring(value))
end

-- Imprime nome Lua, idade 30 etc
```

---
