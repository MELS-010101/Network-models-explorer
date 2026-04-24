# 🌐 Network Models Explorer

<div align="center">
  <p>
    <strong>🇷🇺 Интерактивный визуализатор моделей OSI и TCP/IP</strong>
    <br>
    <strong>🇬🇧 Interactive OSI & TCP/IP Model Visualizer</strong>
  </p>
  <p><em>Один файл. Никаких зависимостей. Работает прямо в браузере.</em></p>
</div>

---

## 🇷🇺 О проекте / 🇬🇧 About

**Network Models Explorer** — это современное одностраничное веб-приложение (SPA), созданное для наглядного изучения сетевого стека. Проект визуализирует, как данные проходят через уровни модели OSI, преобразуются в пакеты, инкапсулируются заголовками протоколов и передаются по физической среде.

**Network Models Explorer** is a modern single-page web application (SPA) designed for intuitive learning of network stacks. It visualizes how data traverses the OSI model layers, gets encapsulated into packets with protocol headers, and is transmitted across physical media.

---

## ⚡ Ключевые особенности / Key Features

| 🇷🇺 Русская версия | 🇬🇧 English Version |
|---|---|
| 📦 **Инкапсуляция** — пошаговая анимация прохождения данных от L7 к L1 с динамическим добавлением заголовков (`HTTP → TLS → Session → TCP → IP → Ethernet`). | 📦 **Encapsulation** — step-by-step animation of data moving from L7 to L1, dynamically adding protocol headers at each stage. |
| 📤 **Декапсуляция** — обратный процесс на стороне приёмника: последовательное снятие заголовков и восстановление исходного Payload. | 📤 **Decapsulation** — the reverse process on the receiving end: stripping headers layer by layer to recover the original payload. |
| ⚠️ **Симуляция ошибок** — эмуляция повреждения кадра, срабатывание FCS/CRC, отбрасывание пакета и автоматическое восстановление через `TCP Retransmission`. | ⚠️ **Error Simulation** — emulates frame corruption, CRC failure, packet drop, and automatic recovery via `TCP Retransmission`. |
| 📊 **Интерактивная сетка** — уровни OSI сгруппированы по зонам TCP/IP. Клик открывает детальную панель (PDU, адресация, протоколы, оборудование). | 📊 **Interactive Grid** — OSI layers mapped to TCP/IP zones. Click reveals detailed info (PDU, addressing, protocols, hardware). |
| 📜 **Журнал событий** — фиксированная панель с автоскроллом, логирующая каждое действие сети в реальном времени. | 📜 **Event Log** — fixed-height panel with auto-scroll, logging every network interaction and system event in real-time. |

---

## 🛠 Технологии / Tech Stack

- **⚛️ React 18** (CDN) — функциональные компоненты, хуки (`useState`, `useEffect`, `useRef`, `useCallback`)
- **🎨 Tailwind CSS** (Play CDN) — утилитарная стилизация, адаптивная сетка, тёмная тема, `glassmorphism`
- **🔤 Babel Standalone** — транспиляция JSX "на лету" без этапа сборки
- **📐 Чистый HTML/JS** — без сборщиков (`Webpack`, `Vite`, `Node.js`), без `package.json`
- **🖼 SVG-иконки** — встроенные векторные элементы, без внешних шрифтов или библиотек

---

## 📦 Как запустить / How to Run

Проект не требует установки зависимостей или компиляции.

1. Скачайте или склонируйте файл `index.html`.
2. Откройте его в любом современном браузере (двойной клик или `File → Open`).
3. Готово! Интернет требуется только для первоначальной загрузки библиотек с CDN.

```bash
# Опционально: запуск через локальный HTTP-сервер
python3 -m http.server 8000
# Перейдите на: http://localhost:8000