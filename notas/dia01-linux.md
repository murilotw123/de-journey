# The Shell - Notes mit lecture 1

## O que é Shell?
- Interface textual para comandar o computador
- Mais poderosa que GUIs (permite fazer tudo)
- **Bash** = Bourne Again Shell (mais comum)
- Todas as shells funcionam basicamente igual

## Estrutura do Prompt
```
missing:~$
```
- `missing` = nome da máquina
- `~` = home directory
- `$` = não é root user

---

## Comandos Básicos

| Comando | Função |
|---------|--------|
| `date` | mostra data/hora |
| `echo` | printa argumentos |
| `pwd` | mostra diretório atual |
| `cd` | muda de diretório |
| `ls` | lista conteúdo |
| `which` | acha onde o programa está |
| `man` | mostra manual de um comando |
| `mkdir` | cria um diretorio |
| `rmdir` | remove um diretorio |
| `mv` | move ou renomeia algo |
| `|(pipe)` | output do da esquerda vira input do da direita |
| `cat` | pega o q tem dentro do arquivo |
| `cp` | copia um arquivo |

---

## Navegação de Diretórios

- `/` = raiz (root) do sistema
- `~` = home
- `.` = diretório atual
- `..` = diretório pai
- **Caminho absoluto** = começa com `/`
- **Caminho relativo** = relativo ao diretório atual

---

## Permissões (ls -l)
```
drwxr-xr-x
```
- **d** = directory
- **rwx** = owner | group | others
  - `r` = read
  - `w` = write (modify)
  - `x` = execute

---

## Redirecionamento & Pipes

### Redirecionamento
```bash
echo hello > hello.txt          # escreve em arquivo
cat < hello.txt                 # lê de arquivo
cat < hello.txt > hello2.txt    # copia
echo hello >> hello.txt         # append
```

### Pipes (|)
```bash
ls -l / | tail -n1              # saída de ls → entrada de tail
curl google.com | grep algo     # encadeia comandos
```

**Importante:** O pipe é feito pelo SHELL, não pelo programa!

---

## sudo vs redirecionamento
```bash
sudo echo 3 > brightness        # ❌ Não funciona (shell não é root)
echo 3 | sudo tee brightness    # ✅ Funciona (tee roda como root)
```

---

## Variáveis importantes
- `$PATH` = lista de diretórios onde shell procura programas
- Separados por `:`

---

## Quick Tips
- Use `-h` ou `--help` para ver flags de um comando
- Use `man comando` para manual completo
- Aspas `""` ou `''` para argumentos com espaços

# Fundamentals of data engineering f1rst cap

- O que diferencia DE de DA e DS?

- O que é o Data Engineering Lifecycle?
