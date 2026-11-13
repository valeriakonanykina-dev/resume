<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Резюме | Валерия Конаныкина</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&family=Fira+Code:wght@400;500;600&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #e2e8f0;
            display: flex;
            justify-content: center;
            padding: 20px;
            font-family: 'Inter', sans-serif;
            -webkit-print-color-adjust: exact;
            print-color-adjust: exact;
        }

        /* Формат А4 */
        .page {
            width: 210mm;
            height: 297mm;
            background: #ffffff;
            position: relative;
            overflow: hidden;
            box-shadow: 0 15px 50px rgba(0,0,0,0.15);
            display: flex;
        }

        /* ЛЕВАЯ КОЛОНКА */
        .left-col {
            width: 32%;
            background: #0f172a;
            color: #f8fafc;
            padding: 40px 25px;
            position: relative;
            z-index: 2;
        }

        .left-col::before {
            content: '';
            position: absolute;
            top: -50px;
            left: -50px;
            width: 200px;
            height: 200px;
            background: radial-gradient(circle, rgba(56, 189, 248, 0.2) 0%, transparent 70%);
            border-radius: 50%;
        }

        .left-col::after {
            content: '';
            position: absolute;
            bottom: 50px;
            right: -30px;
            width: 150px;
            height: 150px;
            background: radial-gradient(circle, rgba(168, 85, 247, 0.15) 0%, transparent 70%);
            border-radius: 50%;
        }

        .abstract-grid {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
            background-size: 20px 20px;
            z-index: -1;
        }

        .section-title-left {
            font-family: 'Fira Code', monospace;
            font-size: 12px;
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #38bdf8;
            margin-bottom: 15px;
            margin-top: 30px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 8px;
        }

        .section-title-left:first-of-type {
            margin-top: 0;
        }

        .contact-item {
            font-size: 12px;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #cbd5e1;
            line-height: 1.4;
        }

        .contact-icon {
            width: 24px;
            height: 24px;
            background: rgba(56, 189, 248, 0.1);
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            flex-shrink: 0;
        }

        .skill-tag {
            display: inline-block;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(56, 189, 248, 0.3);
            color: #e2e8f0;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 11px;
            font-family: 'Fira Code', monospace;
            margin: 0 6px 8px 0;
        }

        .skill-tag.bash {
            background: rgba(56, 189, 248, 0.15);
            border-color: #38bdf8;
            color: #38bdf8;
        }

        .soft-skill {
            font-size: 12px;
            color: #94a3b8;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .soft-skill::before {
            content: '▹';
            color: #a855f7;
            font-size: 14px;
        }

        /* ПРАВАЯ КОЛОНКА */
        .right-col {
            width: 68%;
            padding: 40px 35px;
            position: relative;
            z-index: 2;
        }

        .abstract-shape {
            position: absolute;
            border-radius: 50%;
            opacity: 0.05;
            z-index: -1;
        }

        .shape-1 {
            width: 300px;
            height: 300px;
            background: #a855f7;
            top: -100px;
            right: -100px;
        }

        .shape-2 {
            width: 200px;
            height: 200px;
            background: #38bdf8;
            bottom: 50px;
            left: -50px;
        }

        .header-right {
            margin-bottom: 35px;
        }

        .name {
            font-size: 36px;
            font-weight: 900;
            color: #0f172a;
            line-height: 1.1;
            margin-bottom: 10px;
            letter-spacing: -1px;
        }

        .name span {
            display: block;
            background: linear-gradient(90deg, #0f172a, #475569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .role {
            font-family: 'Fira Code', monospace;
            font-size: 14px;
            color: #a855f7;
            font-weight: 500;
            margin-bottom: 20px;
        }

        .about {
            font-size: 13px;
            color: #475569;
            line-height: 1.6;
            border-left: 3px solid #38bdf8;
            padding-left: 15px;
        }

        .section-title-right {
            font-size: 16px;
            font-weight: 700;
            color: #0f172a;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 20px;
            margin-top: 30px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title-right::before {
            content: '';
            width: 20px;
            height: 3px;
            background: linear-gradient(90deg, #38bdf8, #a855f7);
            border-radius: 2px;
        }

        .section-title-right:first-of-type {
            margin-top: 0;
        }

        .timeline-item {
            position: relative;
            padding-left: 20px;
            margin-bottom: 20px;
            border-left: 2px solid #e2e8f0;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -5px;
            top: 6px;
            width: 8px;
            height: 8px;
            background: #0f172a;
            border-radius: 50%;
        }

        .timeline-date {
            font-family: 'Fira Code', monospace;
            font-size: 11px;
            color: #38bdf8;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .timeline-title {
            font-size: 15px;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 3px;
        }

        .timeline-subtitle {
            font-size: 12px;
            color: #64748b;
            font-style: italic;
            margin-bottom: 6px;
        }

        .timeline-desc {
            font-size: 12px;
            color: #475569;
            line-height: 1.5;
        }

        @media print {
            body {
                background: white;
                padding: 0;
            }
            .page {
                box-shadow: none;
                width: 210mm;
                height: 297mm;
            }
        }

        @page {
            size: A4;
            margin: 0;
        }
    </style>
</head>
<body>

    <div class="page">
        <!-- ЛЕВАЯ КОЛОНКА -->
        <div class="left-col">
            <div class="abstract-grid"></div>
            
            <div class="section-title-left">Контакты</div>
            <div class="contact-item">
                <div class="contact-icon">📞</div>
                <span>+7 (977) 390 58 09</span>
            </div>
            <div class="contact-item">
                <div class="contact-icon">✉️</div>
                <span>valeriakonanykina@gmail.com</span>
            </div>
            <div class="contact-item">
                <div class="contact-icon">📍</div>
                <span>Москва</span>
            </div>
            <div class="contact-item">
                <div class="contact-icon">💻</div>
                <span>github.com/valeria-k</span>
            </div>

            <div class="section-title-left">Hard Skills</div>
            <div>
                <span class="skill-tag bash">Bash (Basic)</span>
                <span class="skill-tag">HTML5 / CSS3</span>
                <span class="skill-tag">VSCodium / VS Code</span>
                <span class="skill-tag">Git / GitHub</span>
                <span class="skill-tag">Алгоритмы</span>
            </div>

            <div class="section-title-left">Soft Skills</div>
            <div class="soft-skill">Быстрая обучаемость</div>
            <div class="soft-skill">Работа в команде</div>
            <div class="soft-skill">Внимание к деталям</div>
            <div class="soft-skill">Аналитическое мышление</div>

            <div class="section-title-left">Языки</div>
            <div class="contact-item">
                <div class="contact-icon">🇷🇺</div>
                <span>Русский — Родной</span>
            </div>
            <div class="contact-item">
                <div class="contact-icon">🇬🇧</div>
                <span>Английский — A1</span>
            </div>
        </div>

        <!-- ПРАВАЯ КОЛОНКА -->
        <div class="right-col">
            <div class="abstract-shape shape-1"></div>
            <div class="abstract-shape shape-2"></div>

            <div class="header-right">
                <h1 class="name"><span>ВАЛЕРИЯ</span> КОНАНЫКИНА</h1>
                <div class="role">Студентка 2 курса | Информационные системы и программирование</div>
                <div class="about">
                    Увлечена IT-разработкой и веб-технологиями. Постоянно изучаю новые инструменты и стремлюсь применять теоретические знания на практике. Ищу производственную практику, чтобы получить реальный опыт работы в команде, познакомиться с корпоративными стандартами и прокачать свои навыки.
                </div>
            </div>

            <div class="section-title-right">Образование</div>
            <div class="timeline-item">
                <div class="timeline-date">2025 — 2029</div>
                <div class="timeline-title">[Люберецкий техникум имени Героя Советского Союза лётчика-космонавта Ю.А. Гагарина]</div>
                <div class="timeline-subtitle">Информационные системы и программирование</div>
                <div class="timeline-desc">
                    2 курс. Изучаю основы программирования, веб-разработку, компьютерные сети, архитектуру ИС и алгоритмизацию.
                </div>
            </div>

            <div class="section-title-right">Учебные проекты</div>
            
            <div class="timeline-item">
                <div class="timeline-date">2026 (2 курс)</div>
                <div class="timeline-title">Разработка учебных веб-сайтов</div>
                <div class="timeline-subtitle">VSCodium, HTML5, CSS3, Git</div>
                <div class="timeline-desc">
                    Верстка и разработка учебных сайтов. Настройка рабочего окружения в VSCodium, подключение расширений, работа с системой контроля версий Git и публикация кода на GitHub.
                </div>
            </div>

            <div class="timeline-item">
                <div class="timeline-date">2025 (1 курс)</div>
                <div class="timeline-title">Лабораторные работы по ОС Linux</div>
                <div class="timeline-subtitle">Linux, Bash, Терминал</div>
                <div class="timeline-desc">
                    Знакомство с операционной системой Linux. Установка ОС, навигация по файловой системе через терминал, базовые команды Bash, работа с правами доступа и пользователями.
                </div>
            </div>

            <div class="section-title-right">Цель практики</div>
            <div class="timeline-item" style="border-left: none; padding-left: 0;">
                <div class="timeline-desc">
                    Закрепить навыки веб-разработки и работы в Linux-среде, познакомиться с реальными IT-проектами, научиться писать чистый код и получить опыт командной работы в профессиональной среде.
                </div>
            </div>

        </div>
    </div>

</body>
</html>
