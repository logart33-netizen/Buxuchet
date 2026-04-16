[bukhuchet_3_day_plan.html](https://github.com/user-attachments/files/26781347/bukhuchet_3_day_plan.html)
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>План обучения: основы бухгалтерского учёта</title>
<style>
:root {
  --day1: #534AB7;
  --day2: #0F6E56;
  --day3: #993C1D;
  --color-text-primary: #1a1a18;
  --color-text-secondary: #5f5e5a;
  --color-text-tertiary: #888780;
  --color-background-primary: #ffffff;
  --color-background-secondary: #f5f4ef;
  --color-border-tertiary: rgba(0,0,0,0.12);
  --border-radius-md: 8px;
  --border-radius-lg: 12px;
  --font-sans: system-ui, -apple-system, sans-serif;
}
@media (prefers-color-scheme: dark) {
  :root {
    --color-text-primary: #e8e6dc;
    --color-text-secondary: #a8a69e;
    --color-text-tertiary: #6e6c66;
    --color-background-primary: #1c1c1a;
    --color-background-secondary: #242422;
    --color-border-tertiary: rgba(255,255,255,0.1);
  }
}
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: var(--font-sans);
  color: var(--color-text-primary);
  background: var(--color-background-primary);
  max-width: 720px;
  margin: 0 auto;
  padding: 24px 20px 48px;
}

.header { padding: 20px 0 8px; }
.header h1 { font-size: 18px; font-weight: 500; color: var(--color-text-primary); }
.header p  { font-size: 13px; color: var(--color-text-secondary); margin-top: 4px; }

.days-nav { display: flex; gap: 8px; margin: 16px 0 0; }
.day-tab { flex: 1; padding: 10px 8px; border-radius: var(--border-radius-md); border: 1px solid var(--color-border-tertiary); cursor: pointer; text-align: center; font-size: 13px; font-weight: 400; color: var(--color-text-secondary); background: var(--color-background-secondary); transition: all .15s; }
.day-tab.active { font-weight: 500; color: #fff; border-color: transparent; }
.day-tab[data-day="1"].active { background: var(--day1); }
.day-tab[data-day="2"].active { background: var(--day2); }
.day-tab[data-day="3"].active { background: var(--day3); }

.day-panel { display: none; padding-top: 16px; }
.day-panel.active { display: block; }

.day-hero { border-radius: var(--border-radius-lg); padding: 16px 20px; margin-bottom: 16px; }
.day-hero[data-c="1"] { background: #EEEDFE; }
.day-hero[data-c="2"] { background: #E1F5EE; }
.day-hero[data-c="3"] { background: #FAECE7; }
.day-hero .label { font-size: 11px; font-weight: 500; letter-spacing: .05em; text-transform: uppercase; margin-bottom: 4px; }
.day-hero[data-c="1"] .label { color: #534AB7; }
.day-hero[data-c="2"] .label { color: #0F6E56; }
.day-hero[data-c="3"] .label { color: #993C1D; }
.day-hero h2 { font-size: 17px; font-weight: 500; color: #1a1a18; margin-bottom: 6px; }
.day-hero p  { font-size: 13px; color: #5f5e5a; line-height: 1.6; }

.timeline { position: relative; padding-left: 28px; }
.timeline::before { content: ''; position: absolute; left: 8px; top: 0; bottom: 0; width: 1px; background: var(--color-border-tertiary); }

.block { position: relative; margin-bottom: 20px; }
.block::before { content: ''; position: absolute; left: -24px; top: 6px; width: 10px; height: 10px; border-radius: 50%; border: 2px solid; background: var(--color-background-primary); }
[data-day="1"] .block::before { border-color: var(--day1); }
[data-day="2"] .block::before { border-color: var(--day2); }
[data-day="3"] .block::before { border-color: var(--day3); }

.block-header { display: flex; align-items: center; gap: 8px; margin-bottom: 8px; }
.block-time { font-size: 11px; color: var(--color-text-tertiary); min-width: 80px; }
.block-type { font-size: 11px; font-weight: 500; padding: 2px 8px; border-radius: 20px; }
.type-theory { background: #EEEDFE; color: #3C3489; }
.type-practice { background: #E1F5EE; color: #085041; }
.type-check  { background: #FAECE7; color: #712B13; }

.block-title { font-size: 14px; font-weight: 500; color: var(--color-text-primary); margin-bottom: 6px; }

.items { list-style: none; }
.items li { font-size: 13px; color: var(--color-text-secondary); line-height: 1.7; padding-left: 14px; position: relative; }
.items li::before { content: '—'; position: absolute; left: 0; color: var(--color-text-tertiary); }

.term-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; margin-top: 6px; }
.term-card { border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 8px 10px; }
.term-card .term { font-size: 12px; font-weight: 500; color: var(--color-text-primary); margin-bottom: 2px; }
.term-card .def  { font-size: 12px; color: var(--color-text-secondary); line-height: 1.5; }

.formula-box { border-radius: var(--border-radius-md); padding: 10px 14px; margin-top: 8px; font-size: 14px; font-weight: 500; text-align: center; }
.formula-box.purple { background: #EEEDFE; color: #3C3489; }
.formula-box.teal   { background: #E1F5EE; color: #085041; }
.formula-box.coral  { background: #FAECE7; color: #712B13; }

.task-box { border-left: 3px solid; border-radius: 0 var(--border-radius-md) var(--border-radius-md) 0; padding: 10px 14px; margin-top: 8px; background: var(--color-background-secondary); }
[data-day="1"] .task-box { border-color: var(--day1); }
[data-day="2"] .task-box { border-color: var(--day2); }
[data-day="3"] .task-box { border-color: var(--day3); }
.task-box .task-label { font-size: 11px; font-weight: 500; text-transform: uppercase; letter-spacing: .05em; margin-bottom: 4px; }
[data-day="1"] .task-box .task-label { color: var(--day1); }
[data-day="2"] .task-box .task-label { color: var(--day2); }
[data-day="3"] .task-box .task-label { color: var(--day3); }
.task-box p { font-size: 13px; color: var(--color-text-secondary); line-height: 1.6; }

.result-pill { display: inline-flex; align-items: center; gap: 6px; padding: 6px 12px; border-radius: 20px; font-size: 13px; margin-top: 10px; }
[data-day="1"] .result-pill { background: #EEEDFE; color: #3C3489; }
[data-day="2"] .result-pill { background: #E1F5EE; color: #085041; }
[data-day="3"] .result-pill { background: #FAECE7; color: #712B13; }
.result-pill::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: currentColor; }

.progress-bar { display: flex; gap: 3px; margin-top: 16px; margin-bottom: 4px; }
.progress-bar span { height: 4px; border-radius: 2px; flex: 1; background: var(--color-border-tertiary); }
[data-day="1"] .progress-bar span.done { background: var(--day1); }
[data-day="2"] .progress-bar span.done { background: var(--day2); }
[data-day="3"] .progress-bar span.done { background: var(--day3); }
.progress-label { font-size: 11px; color: var(--color-text-tertiary); }
</style>
</head>
<body>

<div class="header">
  <h1>План обучения: основы бухгалтерского учёта</h1>
  <p>Полный ноль → уверенная база · 3 дня · 3–4 часа в день</p>
</div>

<div class="days-nav">
  <div class="day-tab active" data-day="1" onclick="switchDay(1)">День 1<br><small style="font-size:11px;opacity:.7">Язык учёта</small></div>
  <div class="day-tab" data-day="2" onclick="switchDay(2)">День 2<br><small style="font-size:11px;opacity:.7">Счета и проводки</small></div>
  <div class="day-tab" data-day="3" onclick="switchDay(3)">День 3<br><small style="font-size:11px;opacity:.7">Вся картина</small></div>
</div>

<!-- ДЕНЬ 1 -->
<div class="day-panel active" data-day="1" id="panel-1">
  <div class="day-hero" data-c="1">
    <div class="label">День 1</div>
    <h2>Язык бухгалтерии: как бизнес превращается в цифры</h2>
    <p>Сегодня ты поймёшь главное: бухгалтерия — это не таблицы. Это способ описать реальность бизнеса на общем языке.</p>
  </div>
  <div class="timeline" data-day="1">
    <div class="block">
      <div class="block-header">
        <span class="block-time">9:00 — 10:30</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 1. Что такое бухгалтерский учёт и зачем он нужен</div>
      <ul class="items">
        <li>Бухучёт = система фиксации всех операций бизнеса в денежном выражении</li>
        <li>Любое движение ценностей → должно быть записано</li>
        <li>Три главных вопроса учёта: Что есть? Откуда взялось? Как изменилось?</li>
        <li>Чем отличается бухгалтерский учёт от управленческого и налогового</li>
        <li>Принцип двойной записи — фундамент всего (каждая операция = 2 стороны)</li>
        <li>Принцип начисления: доход признаётся когда заработан, не когда получены деньги</li>
        <li>Принцип периодичности: учёт делится на периоды (месяц, квартал, год)</li>
        <li>Принцип непрерывности: бизнес работает бесконечно, учёт — тоже</li>
        <li>Принцип денежного измерения: всё переводим в деньги</li>
      </ul>
      <div class="formula-box purple">Бухучёт = зеркало бизнеса в денежном выражении</div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">10:30 — 12:00</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 2. Активы и Пассивы — главное уравнение</div>
      <ul class="items">
        <li><strong>Активы</strong> — всё, чем владеет компания: деньги, товары, оборудование, здания, долги перед компанией</li>
        <li><strong>Пассивы</strong> — всё, за счёт чего это появилось: долги компании + собственный капитал</li>
        <li>Пассивы = Капитал + Обязательства</li>
        <li><strong>Капитал (собственный)</strong> — деньги, вложенные владельцами + накопленная прибыль</li>
        <li><strong>Обязательства</strong> — долги: перед банком (кредит), перед поставщиками (кредиторка), перед налоговой</li>
        <li>Оборотные активы: деньги, товары, дебиторка (быстро превращаются в деньги)</li>
        <li>Внеоборотные активы: оборудование, здания, транспорт (служат долго)</li>
        <li>Краткосрочные обязательства: нужно погасить до 12 месяцев</li>
        <li>Долгосрочные обязательства: погашаем больше года</li>
      </ul>
      <div class="formula-box purple">АКТИВЫ = КАПИТАЛ + ОБЯЗАТЕЛЬСТВА</div>
      <div class="term-grid">
        <div class="term-card"><div class="term">Дебиторская задолженность</div><div class="def">Нам должны клиенты. Это актив — деньги ещё придут.</div></div>
        <div class="term-card"><div class="term">Кредиторская задолженность</div><div class="def">Мы должны поставщикам. Это пассив — обязательство.</div></div>
        <div class="term-card"><div class="term">Основные средства</div><div class="def">Оборудование, здания. Актив, который служит несколько лет.</div></div>
        <div class="term-card"><div class="term">Нераспределённая прибыль</div><div class="def">Прибыль прошлых периодов, не выплаченная владельцам.</div></div>
      </div>
      <div class="task-box">
        <div class="task-label">Задание</div>
        <p>На бумаге: возьми любую торговую компанию (придумай). Напиши что у неё есть (активы) и откуда это взялось (пассивы). Проверь: сумма активов = сумме пассивов.</p>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">13:00 — 14:30</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 3. Доходы, Расходы, Прибыль</div>
      <ul class="items">
        <li><strong>Доход (выручка)</strong> — компания продала товар или оказала услугу. Признаётся в момент продажи, не получения денег.</li>
        <li><strong>Расход</strong> — компания понесла затраты для получения дохода</li>
        <li><strong>Себестоимость</strong> — сколько стоил товар, который мы продали (прямой расход)</li>
        <li><strong>Валовая прибыль</strong> = Выручка − Себестоимость</li>
        <li><strong>Операционные расходы</strong> — аренда, зарплата, реклама (не входят в себестоимость)</li>
        <li><strong>Операционная прибыль (EBIT)</strong> = Валовая прибыль − Операционные расходы</li>
        <li><strong>Чистая прибыль</strong> = Операционная прибыль − Налоги − Проценты по кредитам</li>
        <li>ВАЖНО: Деньги ≠ Прибыль. Продал в долг → прибыль есть, денег нет. Получил аванс → деньги есть, дохода ещё нет.</li>
        <li>Убыток = когда расходы больше доходов</li>
        <li>Рентабельность = Прибыль ÷ Выручка × 100%</li>
      </ul>
      <div class="formula-box purple">Прибыль = Доходы − Расходы</div>
      <div class="term-grid">
        <div class="term-card"><div class="term">Выручка</div><div class="def">Общая сумма от продаж за период. Ещё называют «оборот».</div></div>
        <div class="term-card"><div class="term">Себестоимость</div><div class="def">Что потратили, чтобы сделать/купить то, что продали.</div></div>
        <div class="term-card"><div class="term">EBITDA</div><div class="def">Прибыль до налогов, процентов и амортизации. Показывает реальную операционную силу.</div></div>
        <div class="term-card"><div class="term">Амортизация</div><div class="def">Постепенное списание стоимости оборудования. Расход без выплаты денег.</div></div>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">14:30 — 16:00</span>
        <span class="block-type type-practice">Практика</span>
      </div>
      <div class="block-title">Блок 4. Практика: разбор бизнес-ситуаций на бумаге</div>
      <ul class="items">
        <li>Сценарий А: Вложили 10 000$. Разложи на активы/пассивы.</li>
        <li>Сценарий Б: Купили товар на 6 000$. Что изменилось в активах и пассивах?</li>
        <li>Сценарий В: Продали товар за 9 000$ (покупатель заплатит позже). Где доход? Где долг?</li>
        <li>Сценарий Г: Получили 5 000$ от покупателя. Что изменилось?</li>
        <li>Сценарий Д: Заплатили аренду 1 000$. Это расход? Куда уходит в отчётности?</li>
        <li>После каждого сценария проверяй: Активы = Пассивы?</li>
        <li>Посчитай итоговую прибыль по всем сценариям</li>
        <li>Найди разницу: сколько заработали (прибыль) и сколько денег на счету</li>
      </ul>
      <div class="task-box">
        <div class="task-label">Главный инсайт дня</div>
        <p>Деньги на счету и прибыль — это разные вещи. Когда поймёшь это на практике — уже не ноль.</p>
      </div>
      <div class="result-pill">Итог дня: ты понимаешь язык бухгалтерии</div>
    </div>
  </div>
  <div class="progress-bar" data-day="1">
    <span class="done"></span><span></span><span></span>
  </div>
  <div class="progress-label">День 1 из 3</div>
</div>

<!-- ДЕНЬ 2 -->
<div class="day-panel" data-day="2" id="panel-2">
  <div class="day-hero" data-c="2">
    <div class="label">День 2</div>
    <h2>Счета, проводки и двойная запись — механика учёта</h2>
    <p>Сегодня ты поймёшь как именно фиксируется каждая операция. Это самое важное для работы с 1С.</p>
  </div>
  <div class="timeline" data-day="2">
    <div class="block">
      <div class="block-header">
        <span class="block-time">9:00 — 10:30</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 1. Бухгалтерский счёт — что это такое</div>
      <ul class="items">
        <li>Счёт — это «ячейка» для хранения информации об одном виде ценностей</li>
        <li>Каждый счёт имеет номер (например, 10 — «Материалы», 51 — «Расчётный счёт»)</li>
        <li>Счёт — это Т-образная таблица: левая сторона = Дебет, правая = Кредит</li>
        <li>Сальдо — остаток на счёте (разница между дебетом и кредитом)</li>
        <li>Сальдо начальное — остаток на начало периода</li>
        <li>Обороты — все поступления и списания за период</li>
        <li>Сальдо конечное — остаток на конец периода</li>
        <li>Активные счета: сальдо всегда по дебету (деньги, товары, ОС)</li>
        <li>Пассивные счета: сальдо всегда по кредиту (капитал, долги)</li>
        <li>Активно-пассивные счета: сальдо может быть с обеих сторон (расчёты с контрагентами)</li>
      </ul>
      <div class="term-grid">
        <div class="term-card"><div class="term">Дебет</div><div class="def">Левая сторона счёта. Для активных счетов — поступление. Для пассивных — уменьшение.</div></div>
        <div class="term-card"><div class="term">Кредит</div><div class="def">Правая сторона счёта. Для активных — списание. Для пассивных — увеличение.</div></div>
        <div class="term-card"><div class="term">Оборотно-сальдовая ведомость (ОСВ)</div><div class="def">Таблица по всем счетам: остаток + обороты. Главный отчёт бухгалтера.</div></div>
        <div class="term-card"><div class="term">Аналитика счёта</div><div class="def">Детализация внутри счёта. Например, счёт «Расчёты с клиентами» — по каждому клиенту отдельно.</div></div>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">10:30 — 12:00</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 2. Дебет и Кредит — правильное понимание</div>
      <ul class="items">
        <li>Забудь: «Дебет = плюс, Кредит = минус» — это ломает понимание</li>
        <li>Правильно: каждая операция имеет две стороны — откуда пришло и куда ушло</li>
        <li>Дебет активного счёта = увеличение актива (пришёл товар → дебет «Товары»)</li>
        <li>Кредит активного счёта = уменьшение актива (ушли деньги → кредит «Деньги»)</li>
        <li>Дебет пассивного счёта = уменьшение обязательства (погасили долг → дебет «Долги»)</li>
        <li>Кредит пассивного счёта = увеличение обязательства (взяли кредит → кредит «Кредиты»)</li>
        <li>Золотое правило: сумма всех дебетов = сумме всех кредитов за период</li>
      </ul>
      <div class="formula-box teal">∑ Дебет = ∑ Кредит (всегда, для любой операции)</div>
      <div class="task-box">
        <div class="task-label">Упражнение на бумаге</div>
        <p>Нарисуй Т-счета: «Деньги», «Товары», «Долг покупателя», «Выручка». Проведи по ним операцию: купили товар 100$, продали за 150$ в долг, получили оплату. Смотри как меняются остатки.</p>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">13:00 — 14:30</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 3. Двойная запись и проводки</div>
      <ul class="items">
        <li>Проводка = запись операции в виде: Дебет счёта X — Кредит счёта Y — Сумма</li>
        <li>Каждая операция = минимум одна проводка (часто несколько)</li>
        <li>Купили товар за деньги: Дт «Товары» — Кт «Деньги»</li>
        <li>Купили товар в долг: Дт «Товары» — Кт «Долг поставщику»</li>
        <li>Продали товар: Дт «Долг покупателя» — Кт «Выручка» (и: Дт «Себестоимость» — Кт «Товары»)</li>
        <li>Получили оплату от покупателя: Дт «Деньги» — Кт «Долг покупателя»</li>
        <li>Заплатили поставщику: Дт «Долг поставщику» — Кт «Деньги»</li>
        <li>Начислили зарплату: Дт «Расходы на зарплату» — Кт «Долг перед сотрудниками»</li>
        <li>Выплатили зарплату: Дт «Долг перед сотрудниками» — Кт «Деньги»</li>
        <li>Получили кредит: Дт «Деньги» — Кт «Кредиты»</li>
        <li>Начислили амортизацию: Дт «Амортизация» — Кт «Основные средства»</li>
      </ul>
      <div class="term-grid">
        <div class="term-card"><div class="term">Проводка</div><div class="def">Запись хозяйственной операции: Дт (счёт) — Кт (счёт) — Сумма.</div></div>
        <div class="term-card"><div class="term">Корреспонденция счетов</div><div class="def">Связь между счетами в одной проводке.</div></div>
        <div class="term-card"><div class="term">Сложная проводка</div><div class="def">Один дебет — несколько кредитов (или наоборот). Суммы должны совпадать.</div></div>
        <div class="term-card"><div class="term">Сторно</div><div class="def">Отмена (корректировка) ошибочной проводки обратной записью.</div></div>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">14:30 — 16:00</span>
        <span class="block-type type-practice">Практика</span>
      </div>
      <div class="block-title">Блок 4. Практика: полный цикл операций на бумаге</div>
      <ul class="items">
        <li>Создай таблицу Т-счетов: Деньги / Товары / Расчёты с покупателями / Расчёты с поставщиками / Выручка / Себестоимость / Зарплата к выплате / Расходы на зарплату</li>
        <li>Операция 1: Владелец вложил 10 000$ в бизнес</li>
        <li>Операция 2: Купили товар у поставщика на 6 000$ (ещё не заплатили)</li>
        <li>Операция 3: Оплатили поставщику 4 000$</li>
        <li>Операция 4: Продали товар за 9 000$ в долг, себестоимость 5 000$</li>
        <li>Операция 5: Покупатель оплатил 5 000$</li>
        <li>Операция 6: Заплатили аренду 800$</li>
        <li>Операция 7: Начислили зарплату 2 000$</li>
        <li>Операция 8: Выплатили зарплату 2 000$</li>
        <li>Подсчитай сальдо по каждому счёту. Активы = Пассивы?</li>
        <li>Найди: сколько денег осталось? Сколько должны покупатели? Сколько должны поставщикам?</li>
        <li>Посчитай прибыль через счета доходов и расходов</li>
      </ul>
      <div class="result-pill">Итог дня: ты умеешь читать и составлять проводки</div>
    </div>
  </div>
  <div class="progress-bar" data-day="2">
    <span class="done"></span><span class="done"></span><span></span>
  </div>
  <div class="progress-label">День 2 из 3</div>
</div>

<!-- ДЕНЬ 3 -->
<div class="day-panel" data-day="3" id="panel-3">
  <div class="day-hero" data-c="3">
    <div class="label">День 3</div>
    <h2>Отчётность и полная картина — как читать бизнес</h2>
    <p>Сегодня собираешь всё вместе: три главных отчёта, связь между ними и финальный тест на понимание.</p>
  </div>
  <div class="timeline" data-day="3">
    <div class="block">
      <div class="block-header">
        <span class="block-time">9:00 — 10:30</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 1. Три главных отчёта</div>
      <ul class="items">
        <li><strong>Баланс</strong> — фото компании на дату: что есть и откуда. Всегда: Активы = Пассивы</li>
        <li>Баланс показывает СОСТОЯНИЕ, не движение</li>
        <li><strong>ОПУ / P&amp;L</strong> — фильм за период: сколько заработали и потратили</li>
        <li>ОПУ: Выручка → Себестоимость → Валовая прибыль → Операционные расходы → Операционная прибыль → Налоги → Чистая прибыль</li>
        <li><strong>ОДС (Cash Flow)</strong> — сколько денег пришло и ушло реально</li>
        <li>ОДС: операционная / инвестиционная / финансовая деятельность</li>
        <li>Связь: чистая прибыль из ОПУ увеличивает капитал в балансе. Деньги в ОДС = деньги в балансе.</li>
        <li>ОСВ — внутренний отчёт бухгалтера, основа для всех трёх</li>
      </ul>
      <div class="term-grid">
        <div class="term-card"><div class="term">Баланс</div><div class="def">Срез на дату. Актив = Пассив. Показывает финансовое положение.</div></div>
        <div class="term-card"><div class="term">P&L / ОПУ</div><div class="def">За период. Выручка минус расходы = прибыль. Показывает эффективность.</div></div>
        <div class="term-card"><div class="term">Cash Flow / ОДС</div><div class="def">Движение денег. Прибыльная компания может иметь кассовый разрыв.</div></div>
        <div class="term-card"><div class="term">Кассовый разрыв</div><div class="def">Прибыль есть, а денег нет — все в долгах дебиторов или товарах.</div></div>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">10:30 — 12:00</span>
        <span class="block-type type-theory">Теория</span>
      </div>
      <div class="block-title">Блок 2. Участки учёта — как устроен бухгалтерский отдел</div>
      <ul class="items">
        <li><strong>Учёт денег:</strong> касса, расчётный счёт, банковская выписка, кассовая книга, ПКО/РКО</li>
        <li><strong>Учёт товаров и склада:</strong> приходная накладная, расходная накладная, инвентаризация, FIFO</li>
        <li><strong>Учёт покупок:</strong> поступление товаров/услуг, счёт-фактура, акт выполненных работ</li>
        <li><strong>Учёт продаж:</strong> счёт на оплату, счёт-фактура исходящая, акт, реализация</li>
        <li><strong>Расчёты с клиентами:</strong> дебиторская задолженность, акт сверки, авансы полученные</li>
        <li><strong>Расчёты с поставщиками:</strong> кредиторская задолженность, авансы выданные</li>
        <li><strong>Учёт зарплаты:</strong> начисление, удержания (НДФЛ), выплата, социальные взносы</li>
        <li><strong>Учёт основных средств:</strong> принятие к учёту, амортизация, списание</li>
        <li><strong>Закрытие месяца:</strong> распределение расходов, расчёт себестоимости, расчёт налогов</li>
      </ul>
      <div class="term-grid">
        <div class="term-card"><div class="term">Счёт-фактура</div><div class="def">Документ для учёта НДС. Основание для вычета налога у покупателя.</div></div>
        <div class="term-card"><div class="term">Акт сверки</div><div class="def">Документ, подтверждающий взаимные расчёты с контрагентом.</div></div>
        <div class="term-card"><div class="term">Авансы полученные</div><div class="def">Деньги от клиента до отгрузки. Это обязательство (пассив), не доход.</div></div>
        <div class="term-card"><div class="term">НДС к уплате</div><div class="def">НДС с продаж минус НДС с покупок = сумма к уплате в бюджет.</div></div>
      </div>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">13:00 — 14:30</span>
        <span class="block-type type-practice">Практика</span>
      </div>
      <div class="block-title">Блок 3. Практика: составить три отчёта из операций дня 2</div>
      <ul class="items">
        <li>Возьми 8 операций из Дня 2 с уже составленными проводками</li>
        <li>Составь Баланс на конец периода: активы (деньги, товары, дебиторка) и пассивы (долг поставщику, капитал)</li>
        <li>Составь ОПУ: выручка 9 000$ − себестоимость 5 000$ − аренда 800$ − зарплата 2 000$ = прибыль?</li>
        <li>Составь упрощённый ОДС: приходы и расходы денег</li>
        <li>Проверь: деньги в балансе = деньги в ОДС?</li>
        <li>Найди: прибыль ≠ деньги. Объясни сам себе почему</li>
        <li>Прочитай ОСВ из Дня 2. Найди в ней все три отчёта «внутри»</li>
      </ul>
    </div>
    <div class="block">
      <div class="block-header">
        <span class="block-time">14:30 — 16:00</span>
        <span class="block-type type-check">Финальный тест</span>
      </div>
      <div class="block-title">Блок 4. Финальный тест — проверка всей базы</div>
      <ul class="items">
        <li>Объясни своими словами: что такое двойная запись и почему без неё нельзя</li>
        <li>Назови 5 активов и 5 пассивов любой компании</li>
        <li>Составь проводки: получили кредит 20 000$ / купили оборудование / начислили амортизацию</li>
        <li>Что такое кассовый разрыв — приведи пример из реального бизнеса</li>
        <li>Чем отличается баланс от P&L? Когда смотришь один, когда другой?</li>
        <li>Компания заработала 1 000 000$ выручки и показала прибыль 50 000$, но у неё нет денег. Почему?</li>
        <li>Клиент говорит: «у меня не сходится ОСВ». Что первым делом проверяешь?</li>
        <li>Авансы полученные — это актив или пассив? Почему?</li>
        <li>Продали товар в кредит. В каком отчёте это уже отразится, а в каком — ещё нет?</li>
        <li>Объясни амортизацию так, чтобы понял школьник</li>
      </ul>
      <div class="task-box">
        <div class="task-label">Критерий успеха</div>
        <p>8 из 10 — база есть, можно идти в курс по 1С. 10 из 10 — отлично. Меньше 6 — вернись к конкретным блокам.</p>
      </div>
      <div class="result-pill">Итог 3 дней: ты мыслишь категориями учёта</div>
    </div>
  </div>
  <div class="progress-bar" data-day="3">
    <span class="done"></span><span class="done"></span><span class="done"></span>
  </div>
  <div class="progress-label">День 3 из 3 — финиш</div>
</div>

<script>
function switchDay(n) {
  document.querySelectorAll('.day-panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.day-tab').forEach(t => t.classList.remove('active'));
  document.getElementById('panel-' + n).classList.add('active');
  document.querySelector('.day-tab[data-day="' + n + '"]').classList.add('active');
}
</script>
</body>
</html>
