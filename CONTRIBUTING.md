# Как внести лепту в MEPhI Docs 😎

Спасибо, что вы решили помочь MEPhI Docs, внеся ~~свой вклад~~ свою лепту в него!

## 👶 Как начать?

Вы таки ~~с долей сомнения~~ уверенно решили сделать какое-то изменеие, но как начать вы не знаете? 😫

Не бойтесь! Я сейчас вам всё расскажу! Всё насколько же просто, как посчитать до `5`!

1) [~~форкни~~ вилкани репозиторий](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository) 🍴
2) [создай новую ветку](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository#creating-a-branch-via-the-branches-overview) 🌿
3) [склонируй репозиторий](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#cloning-a-repository) 🔽
4) поменяй что-нибудь ➕
5) [~~сделай pull request (pr)~~ запроси вытягивание](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request#creating-the-pull-request) 🤝

Да, в ссылках всё на высшем эльфийском ... а чего ты хотел?! Такова жизнь!

![Improvise. Adapt. Overcome ☝](docs/_static/images/improvise_adapt_overcome.jpg)

## 📈 Как *возвести* документацию?

Когда вы сделали изменения в каких-то документах, было бы хорошо сначала увидеть конечный результат, прежде чем загружать изменения на всеобщее обозрение 😳

Именно для этой цели вы можете ~~собрать~~ возвести документацию ~~локально~~ у себя дома ☕

Я предположу, что если вы сделали какие-то изменения, то у вас уже скачан репозиторий 🤔  
(а если всё ещё не скачан, то посмотрите предыдущий раздел ⤴)

<br>

Первым делом зайдите в корневую папку репозитория, а потом пропишите в консоли ⌨

```console
python -m pip install -r requirements.txt
```

😅 Ах да, совсем забыл, что для этого шага вам понадобиться питон. Если что скачайте его из [python.org](https://www.python.org/)

Эта команда скачает всё, что вам понадобится при возведении! 😉

<br>

Когда вы всё скчаете, запускайте эту команду:

```console
make html
```

Эта команда создаст папку `build` c папкой `html` внутри, заходите туда и открывайте `index.html`

Это главная страница сайта, оттуда вы уже сможете найти свой путь к нужному документу 🤗

## ☝ Указания

Наши правила просты

- Отсебятине/интернетной копипасте скажем нет! Только констпекты лекций/семинаров 😇
- Если надо использовать уже законспектированные понятия, то берём их, а не свои 😘

И ещё

- Если вашего направления нет в списке, а вы хотите, чтобы был - создавайте новую папку и кидайте доки туда 📁

## ✍ Как писать документы?

![Я ВИДЕЛ НЕКОТОРОЕ ДЕРЬМО (ГАРРИ ПОТТЕР)](docs/_static/images/wonky_ive_seen_some_shit.jpg)

Не думайте

> "Ну это же MarkDown, а не код, тут не надо писать красиво 💅"

Надо! Но как? А вот так:

- Старайтесь выдерживать один стиль. Одинаковые штуки прописывайте одинаково 🙃

- Старайтесь не писать много операторов подряд без пробельных символов, чтобы TeX читался лучше.
    Например, вместо `F\simeq\FF_{p^m}\implies\RR^n\simeqS` лучше написать `F \simeq \FF_{p^m} \implies \RR^n \simeq S` 

- Обычно для стрелок лучше использовать следующие команды:
  - вместо `\Longrightarrow` ( $\Longrightarrow$ ) и `\Rightarrow` ( $\Rightarrow$ ) лучше использовать `\implies`
  - вместо `\Leftrightarrow` ( $\Leftrightarrow$ ) &mdash; `\iff` или `\ident`
  - вместо `\rightarrow` ( $\rightarrow$ ) &mdash; `\to`

- Ставьте пробел после запятой

- Для множеств стоит использовать запись вида `\set{f(x) \in A}`

- Для определения функций стоит использовать `\colon` вместо `:` для правильных пробелов около `:`  
  Например `f \colon \N \to \N`.

- Вместо `tan`, `cos`, `tg`, `sup`, `lim` используйте `\tan`, `\cos`, `\tg`, `\sup`, `\lim` и так далее

- Для матриц используйте `\mat`, `\det`, `\pmat` (разные скобки) - `\mat{a & b \\ c & d}`

- И в целом, если вам надо написать `\begin{X} ... \end{X}` рекомендуем писать `\block{X}{...}`, это легче читается и редактируется

- Если в скобки надо обернуть выражение, которое по размеру выше стандартных скобок, используйте конструкции вида `\left\(...\right\)`, а не просто `(...)`.
  Но не стоит их использовать везде, читать или изменять такой код сложнее, тем более `\set`, `\brakets` и `\sharpbrakets` точно также моугт оборочивать высокие выражения. 😁

  Также, из-за обычных скобок могут быть проблемы с пробелами, например

  ```latex
  \begin{align*}
  & U\left(S\left(n\right),x\right) \\
  & U\left(S\left(n\right), x\right) \\
  & U\left(S(n), x\right) \\
  & U(S(n), x)
  \end{align*}
  ```

  $$
  \begin{align*}
  & U\left(S\left(n\right),x\right) \\
  & U\left(S\left(n\right), x\right) \\
  & U\left(S(n), x\right) \\
  & U(S(n), x)
  \end{align*}
  $$

- Если необходимо быстро найти обозначение какого-то математического символа, можно использовать [detexify](https://detexify.kirelabs.org/classify.html), [этот](https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols) и [этот](http://tug.ctan.org/info/symbols/comprehensive/symbols-a4.pdf) ресурсы.

- Дополнительные сокращения определены в [preamble.sty](docs/preamble.sty)
