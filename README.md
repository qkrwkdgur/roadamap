<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI/SW 진로 포트폴리오</title>
    <style>
        /* 기본 스타일 및 다크모드 설정 */
        :root {
            --bg-dark: #0a0b10;
            --bg-navy: #161b22;
            --accent-green: #39ff14;
            --accent-blue: #00f0ff;
            --text-white: #e6edf3;
            --text-gray: #8b949e;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, Roboto, sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* 내비게이션 바 */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 11, 16, 0.8);
            backdrop-filter: blur(10px);
            padding: 1.5rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 1px solid rgba(0, 240, 255, 0.2);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--accent-blue);
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--text-white);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--accent-green);
        }

        /* 섹션 공통 스타일 */
        section {
            padding: 100px 10% 60px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--accent-blue);
            text-align: center;
            position: relative;
        }

        h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--accent-green);
            margin: 10px auto;
        }

        /* 메뉴 1: 미래 유망 직무 */
        .job-card {
            background: var(--bg-navy);
            padding: 2.5rem;
            border-radius: 20px;
            border-left: 5px solid var(--accent-green);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .job-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--accent-green);
        }

        .job-card ul {
            list-style: none;
        }

        .job-card li {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .job-card li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: var(--accent-blue);
        }

        /* 메뉴 2: 핵심 필수 역량 */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            transition: transform 0.3s;
            border: 1px solid rgba(0, 240, 255, 0.1);
        }

        .skill-item:hover {
            transform: translateY(-10px);
            border-color: var(--accent-green);
        }

        .skill-item h4 {
            color: var(--accent-blue);
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        /* 메뉴 3: 세로형 타임라인 로드맵 */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 2px;
            background: var(--accent-blue);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1px;
        }

        .container {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
        }

        .container::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -10px;
            background-color: var(--bg-dark);
            border: 4px solid var(--accent-green);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }

        .left { left: 0; }
        .right { left: 50%; }
        .right::after { left: -10px; }

        .content {
            padding: 20px 30px;
            background: var(--bg-navy);
            position: relative;
            border-radius: 15px;
        }

        .content h3 {
            color: var(--accent-green);
            margin-bottom: 10px;
        }

        /* 반응형 */
        @media screen and (max-width: 768px) {
            nav { padding: 1rem; }
            nav ul li { margin-left: 1rem; font-size: 0.9rem; }
            .timeline::after { left: 31px; }
            .container { width: 100%; padding-left: 70px; padding-right: 25px; }
            .container::after { left: 21px; }
            .right { left: 0%; }
        }

        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">Future AI Dev</div>
        <ul>
            <li><a href="#jobs">유망 직무</a></li>
            <li><a href="#skills">필수 역량</a></li>
            <li><a href="#roadmap">4년 로드맵</a></li>
        </ul>
    </nav>

    <!-- 메뉴 1: 미래 유망 직무 (마크다운 1번 내용 기반) -->
    <section id="jobs">
        <h2>미래 유망 직무</h2>
        <div class="job-card">
            <h3>소버린 클라우드 및 도메인 AI 전문가 [1]</h3>
            <p style="margin-bottom: 1.5rem; color: var(--text-gray);">국가별 규제와 주권 요구에 맞춰 인프라를 배치하고, 특정 산업 데이터를 활용하여 정확도와 신뢰성을 높인 전문 AI 모델을 구축하는 전문가입니다 [1-3].</p>
            <ul>
                <li><strong>핵심 역할:</strong> 지오패트리에이션(Geopatriation) 전략 수립 및 워크로드 이전 [3]</li>
                <li><strong>전문 분야:</strong> 기밀 컴퓨팅(Confidential Computing) 기반 데이터 보호 </li>
                <li><strong>기술 도구:</strong> DSLM(도메인 특화 지능) 구축 및 RAG 아키텍처 설계 [1, 4]</li>
            </ul>
        </div>
    </section>

    <!-- 메뉴 2: 핵심 필수 역량 (마크다운 2번 내용 기반) -->
    <section id="skills">
        <h2>핵심 필수 역량</h2>
        <div class="skills-grid">
            <div class="skill-item">
                <h4>AI 네이티브 오케스트레이션 [5]</h4>
                <p>AI 도구를 일상적으로 활용하며, 깃허브 코파일럿 등 AI 코딩 어시스턴트를 통한 개발 생산성 극대화 [5, 6].</p>
            </div>
            <div class="skill-item">
                <h4>멀티에이전트 시스템 (MAS) [6]</h4>
                <p>여러 자율 에이전트가 협업하여 복잡한 목표를 달성하는 시스템 설계 및 에이전틱 루프 감독 [6].</p>
            </div>
            <div class="skill-item">
                <h4>데이터 아키텍처 & 문맥 관리 [5]</h4>
                <p>NoSQL 및 벡터 데이터베이스 환경에서 데이터와 메타데이터를 구조화하고 시맨틱 인덱싱을 수행하는 능력 [5].</p>
            </div>
            <div class="skill-item">
                <h4>디지털 신뢰 및 보안 [6]</h4>
                <p>프롬프트 주입 방어 및 디지털 출처 증명(Digital Provenance)을 통한 AI 결과물의 진위 검증 기술 [6].</p>
            </div>
        </div>
    </section>

    <!-- 메뉴 3: 나의 4년 로드맵 (마크다운 3번 내용 기반) -->
    <section id="roadmap">
        <h2>나의 4년 로드맵</h2>
        <div class="timeline">
            <div class="container left">
                <div class="content">
                    <h3>1학년: AI 활용 및 CS 기초 [7]</h3>
                    <p>Python/Java 기초, 자료구조 및 알고리즘 학습. AI 코딩 어시스턴트 활용 능력(AI Fluency) 확보 [7].</p>
                </div>
            </div>
            <div class="container right">
                <div class="content">
                    <h3>2학년: 데이터 및 문맥 보안 [7]</h3>
                    <p>RDBMS/NoSQL 데이터 모델링, API 보안 및 RAG 시스템 구축을 통한 데이터 거버넌스 이해 [7].</p>
                </div>
            </div>
            <div class="container left">
                <div class="content">
                    <h3>3학년: 보안 플랫폼 고도화 [8]</h3>
                    <p>AI 특화 위험(프롬프트 주입 등) 방어 기술 습득 및 AI 보안 관제 대시보드 제작 프로젝트 수행 [8].</p>
                </div>
            </div>
            <div class="container right">
                <div class="content">
                    <h3>4학년: 디지털 신뢰 & 거버넌스 [4]</h3>
                    <p>기밀 컴퓨팅 및 소버린 클라우드 전략 설계. 기업용 디지털 신뢰 관리 플랫폼 캡스톤 수행 [4].</p>
                </div>
            </div>
        </div>
    </section>

    <footer style="text-align: center; padding: 2rem; color: var(--text-gray); font-size: 0.8rem;">
        &copy; 2026 AI/SW Career Portfolio. All rights reserved.
    </footer>

</body>
</html>
