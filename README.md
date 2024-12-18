<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>가경국민체육센터 기술 매뉴얼</title>
    <style>
    /* Reset 기본 스타일 (브라우저 기본값 초기화) */
body, h1, h2, h3, h4, h5, h6, p, ul, ol, li, table, th, td, img {
    margin: 0; /* 기본 margin 값 제거 */
    padding: 0; /* 기본 padding 값 제거 */
    border: 0; /* 기본 border 값 제거 */
    font-size: 100%; /* 기본 font-size 값 설정 */
    vertical-align: baseline; /* 기본 수직 정렬 방식 설정 */
    box-sizing: border-box; /* padding과 border를 요소 크기 계산에 포함시킴 */
}

/* Reset 스타일 후 기본 레이아웃 */
body {
    font-family: Arial, sans-serif; /* 기본 글꼴 설정 */
    line-height: 1.6; /* 줄 간격 설정 */
    background-color: #f5f5f5; /* 배경색 설정 */
    color: #333; /* 기본 텍스트 색상 설정 */
    padding: 20px; /* 페이지 내 여백 설정 */
}

/* 컨테이너 */
.container {
    display: flex; /* flexbox 레이아웃을 사용 */
    margin: 20px; /* 외부 여백 설정 */
}

/* 목차 (사이드바) */
.sidebar {
    position: fixed; /* 고정 위치 */
    top: 0; /* 상단에 고정 */
    left: -3cm; /* 기본적으로 숨겨짐, 화면 왼쪽으로 3cm만큼 숨겨놓음 */
    width: 3cm; /* 사이드바 너비 */
    height: 100vh; /* 화면 전체 높이 */
    background-color: #f9f9f9; /* 배경색 설정 */
    border: 1px solid #ddd; /* 테두리 설정 */
    padding: 10px; /* 내측 여백 설정 */
    overflow-y: auto; /* 내용이 넘칠 경우 세로 스크롤바 추가 */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* 그림자 효과 */
    transition: left 0.3s ease; /* 마우스를 올렸을 때 부드럽게 펼쳐지도록 설정 */
}

/* 사이드바가 펼쳐졌을 때 */
.sidebar.show {
    left: 0; /* 왼쪽으로 0으로 이동하여 화면에 표시 */
}

/* 사이드바에 마우스를 올렸을 때 */
.sidebar:hover {
    left: 0; /* 마우스가 사이드바에 있을 때 왼쪽으로 펼쳐짐 */
}

/* 사이드바 안의 내용 스타일 */
.sidebar h2 {
    font-size: 1.2em;
    text-align: center;
    color: #0056b3;
    margin-bottom: 10px;
}

/* 목록 스타일 */
.sidebar ul {
    list-style: none;
    padding-left: 0;
}

.sidebar ul li {
    margin: 10px 0;
    font-size: 0.9em;
}

.sidebar ul li a {
    text-decoration: none;
    color: #333;
    display: block;
    padding: 5px 10px;
    border-radius: 5px;
    transition: background-color 0.3s;
}

/* 마우스 오버 시 링크의 배경색 변경 */
.sidebar ul li a:hover {
    background-color: #0056b3;
    color: #ffffff;
}

/* 메인 콘텐츠 */
.main-content {
    width: 87%; /* 메인 콘텐츠 너비 설정 */
    margin-left: 13%; /* 사이드바가 차지한 공간만큼 왼쪽 여백 설정 */
    padding: 20px; /* 내측 여백 설정 */
    background-color: #ffffff; /* 배경색 설정 */
    border: 1px solid #ddd; /* 테두리 설정 */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* 그림자 효과 추가 */
    position: relative; /* 상대 위치로 설정 */
    overflow-y: auto; /* 내용이 넘칠 경우 세로 스크롤바 추가 */
    height: calc(100vh - 10px); /* 화면 높이에서 10px을 뺀 값으로 콘텐츠 영역 높이 설정 */
}

/* 제목 */
.main-content h1 {
    background-color: #0056b3; /* 제목 배경색 설정 */
    color: #ffffff; /* 제목 텍스트 색상 설정 */
    text-align: center; /* 제목 가운데 정렬 */
    padding: 15px; /* 제목 내측 여백 설정 */
    font-size: 2em; /* 제목 글꼴 크기 설정 */
    margin-bottom: 20px; /* 제목 아래 여백 설정 */
}

.main-content h6 {
    background-color: #0056b3; /* 배경색 설정 */
    color: white; /* 텍스트 색상 설정 */
    padding: 10px; /* 내측 여백 설정 */
    float: right; /* 오른쪽 정렬 */
    font-size: 0.8em; /* 글꼴 크기 설정 */
    margin: 0; /* 마진 제거 */
}

/* 기본 텍스트 */
.main-content p {
    margin: 10px 0; /* 텍스트 상하 여백 설정 */
    line-height: 1.8; /* 줄 간격 설정 */
}

/* 테이블 */
.main-content table {
    width: 100%; /* 테이블 너비를 100%로 설정 */
    border-collapse: collapse; /* 테이블 셀 경계가 겹치지 않도록 설정 */
    margin: 20px 0; /* 테이블 상하 여백 설정 */
}

.main-content table th,
.main-content table td {
    border: 1px solid #ccc; /* 테이블 셀 경계선 설정 */
    padding: 10px; /* 셀 내측 여백 설정 */
    text-align: left; /* 텍스트 왼쪽 정렬 */
}

.main-content table th {
    background-color: #f1f1f1; /* 헤더 셀 배경색 설정 */
    font-weight: bold; /* 헤더 셀 텍스트 굵게 설정 */
    text-align: center; /* 헤더 셀 텍스트 가운데 정렬 */
}

.main-content table td {
    background-color: #ffffff; /* 데이터 셀 배경색 설정 */
}

/* 이미지 */
.main-content img {
    max-width: 100%; /* 이미지 최대 너비를 100%로 설정 */
    height: auto; /* 이미지의 비율을 유지한 채로 높이를 자동 조정 */
    margin: 10px 0; /* 이미지 상하 여백 설정 */
}

/* 업데이트 현황 테이블 스타일 */
#updateContainer, #facilityContainer {
    max-height: 300px; /* 고정 높이 설정 */
    overflow-y: auto; /* 세로 스크롤 활성화 */
    margin: 0 auto;
    width: 80%;
    border: 1px solid #ddd;
    padding: 10px;
    margin-top: 10px;
}

/* 숨겨진 콘텐츠 스타일 */
.hidden {
    display: none;
}

/* 펼치기/접기 버튼 스타일 */
.toggle-button {
    padding: 10px;
    background-color: #ffffff; /* 배경색을 흰색으로 설정 */
    color: #333; /* 텍스트 색상 */
    border: 1px solid #ddd; /* 테두리 설정 */
    cursor: pointer; /* 마우스를 올리면 손 모양으로 바뀌도록 설정 */
    font-size: 16px; /* 버튼 텍스트 크기 설정 */
    width: auto; /* 버튼 너비를 콘텐츠에 맞게 설정 */
    transition: background-color 0.3s, border 0.3s; /* 배경색과 테두리 색상에 부드러운 전환 효과 적용 */
}

/* 버튼 마우스 오버 시 스타일 */
.toggle-button:hover {
    background-color: #f1f1f1; /* 버튼 배경색을 밝은 회색으로 변경 */
    border-color: #bbb; /* 버튼 테두리 색을 어두운 회색으로 변경 */
}

/* 업데이트 현황 [펼치기·접기] 버튼 스타일 */
.toggle-button {
    padding: 10px;
    background-color: #ffffff; /* 배경색을 흰색으로 설정 */
    color: #333; /* 텍스트 색상 */
    border: 1px solid transparent; /* 초기 상태에서 테두리는 투명하게 설정 */
    cursor: pointer; /* 마우스를 올리면 손 모양으로 바뀌도록 설정 */
    font-size: 16px; /* 버튼 텍스트 크기 설정 */
    width: auto; /* 버튼 너비를 콘텐츠에 맞게 설정 */
    transition: background-color 0.3s, border-color 0.3s, box-shadow 0.3s; /* 배경색, 테두리 색상, 그림자 전환 효과 */
    border-radius: 5px; /* 테두리 둥글게 */
}

/* 버튼에 마우스를 올렸을 때 파란색 배경과 테두리 효과 */
.toggle-button:hover {
    background-color: #0056b3; /* 배경색을 파란색으로 변경 */
    color: white; /* 텍스트 색상 흰색으로 변경 */
    border-color: #0056b3; /* 테두리 색상을 파란색으로 변경 */
    box-shadow: 0 0 5px rgba(0, 86, 179, 0.8); /* 파란색 테두리 효과 */
}

/* 접기/펼치기 화살표 스타일 */
.arrow {
    display: inline-block;
    margin-right: 5px;
    font-size: 16px; /* 화살표 크기 설정 */
    transition: transform 0.3s ease; /* 부드럽게 회전하도록 설정 */
}

/* 펼침 상태 (화살표가 90도 회전하며 아래로 펼쳐짐) */
.collapsed {
    transform: rotate(0deg); /* 오른쪽 화살표 */
}

/* 펼쳤을 때 (화살표가 90도 회전하여 아래쪽을 가리킴) */
.expanded {
    transform: rotate(90deg); /* 아래쪽 화살표로 회전 */
}

/* 목차 항목에 마우스를 올렸을 때 강조 효과 */
ul li h3 {
    display: inline-block; /* 텍스트만큼 너비가 자동으로 설정되도록 함 */
    padding: 5px 10px; /* 좌우 여백만 설정 (상하 여백은 없애고) */
}

ul li h3:hover {
    background-color: #0056b3; /* 배경색을 파란색으로 변경 */
    color: white; /* 텍스트 색상은 흰색으로 변경 */
    border-radius: 5px; /* 테두리 둥글게 처리 */
    border: 1px solid #0056b3; /* 테두리를 파란색으로 설정 */
}

/* 목차 항목의 링크 텍스트에 마우스를 올렸을 때 효과 */
ul li h3:hover .arrow {
    color: white; /* 화살표 색상을 흰색으로 변경 */
}

/* 사이드바가 마우스를 올렸을 때 펼쳐지는 효과 */
.sidebar {
    left: -3cm; /* 사이드바가 숨겨짐 */
    width: 3cm; /* 사이드바 너비 */
    height: 100vh;
    transition: left 0.3s ease; /* 마우스를 올렸을 때 부드럽게 펼쳐짐 */
}

.sidebar:hover {
    left: 0; /* 마우스가 사이드바에 있을 때 펼쳐짐 */
}

/* 모바일 반응형 스타일 */
@media (max-width: 768px) {
    .sidebar {
        width: 100%; /* 모바일에서는 사이드바 너비를 100%로 설정 */
    }
}
</style>

</head>
<body>


    <div class="container">
        <!-- 목차 영역 -->
        <div class="sidebar">
            <a id="section2.2.5" href="file:///C:/Users/best/Desktop/공유폴더/2.%20기술분야/21.%20매뉴얼/매뉴얼/통합운영매뉴얼%20v1.04.html" target="_blank">전화면으로</a>
            <h2>목차</h2>
            <ul>
                <li><a href="#section1" onclick="toggleSection('skill1')"><span class="highlight">1.</span> 기계</a>
                    <ul>
                        <li style="margin-left: 10px;"><a href="#section1-1" onclick="toggleSection('skill 1.1.')"><span class="highlight">1.1</span> 보일러</a></li>
                        <li style="margin-left: 10px;"><a href="#section1-2" onclick="toggleSection('skill 1.2.')"><span class="highlight">1.2</span> 수영장 제어설비</a></li>
                        <li style="margin-left: 10px;"><a href="#section1-3" onclick="toggleSection('skill 1.3.')"><span class="highlight">1.3</span> 온수가열기</a></li>
                        <li style="margin-left: 10px;"><a href="#section1-4" onclick="toggleSection('skill 1.4.')"><span class="highlight">1.4</span> 공조기</a></li>
                    </ul>
                </li>

                <li><a href="#section2" onclick="toggleSection('skill2')"><span class="highlight">2.</span> 전기</a>
                    <ul>
                        <li style="margin-left: 10px;"><a href="#section2-1" onclick="toggleSection('skill 2.1.')"><span class="highlight">2.1.</span> 정전</a></li>
                        <li style="margin-left: 10px;"><a href="#section2-1" onclick="toggleSection('skill 2.2.')"><span class="highlight">2.2.</span> 복전</a></li>
                        <li style="margin-left: 10px;"><a href="#section2-1" onclick="toggleSection('skill 2.3.')"><span class="highlight">2.3.</span> 기타</a></li>
                            <ul style="margin-left: 10px;"> <!-- 내어쓰기 적용 -->
                                <li style="margin-left: 0px;"><a href="#section2-1-1" onclick="toggleSection('skill 2.3.1.')"><span class="highlight">2.3.1.</span> 기타 주요 업무</a></li>
                            </ul>
                    </ul>   
                </li>
                <li><a href="#section2" onclick="toggleSection('skill3')"><span class="highlight">3.</span> 소방</a>
                    <ul>
                        <li style="margin-left: 10px;">
                            <a href="#section2-1" onclick="toggleSection('admin0')"><span class="highlight">3.1.</span> 화재감지기 작동 및<br><span style="margin-left: 21px; line-height: 1.2;">화재발생 대응</span></a>
                        </li>
                    </ul>
                </li>

                <li><a href="#section2" onclick="toggleSection('skill4')"><span class="highlight">4.</span> 수질</a>
                    <ul>
                        <li style="margin-left: 10px;"><a href="#section4-1" onclick="toggleSection('admin0')"><span class="highlight">4.1.</span> 수영장 수질 자동측정 장치</a>
                        <li style="margin-left: 10px;"><a href="#section4-1" onclick="toggleSection('admin0')"><span class="highlight">4.2.</span> 수영장 염소 측정</a>
                            <ul style="margin-left: 10px;"> <!-- 내어쓰기 적용 -->
                                <li style="margin-left: 0px;"><a href="#section4-2-1" onclick="toggleSection('cheongju1')"><span class="highlight">4.2.1.</span> 비색계 측정</a></li>
                                <li style="margin-left: 0px;"><a href="#section4-2-2" onclick="toggleSection('cheongju1')"><span class="highlight">4.2.2.</span> 시약 측정</a></li>
                            </ul>
                        <li style="margin-left: 10px;"><a href="#section4-3" onclick="toggleSection('admin0')"><span class="highlight">4.3.</span> 수영장 약품 관리</a>
                            <ul style="margin-left: 10px;"> <!-- 내어쓰기 적용 -->
                                <li style="margin-left: 0px;"><a href="#section4-3-1" onclick="toggleSection('cheongju1')"><span class="highlight">4.3.1.</span> 종류</a></li>
                                <li style="margin-left: 0px;"><a href="#section4-3-2" onclick="toggleSection('cheongju1')"><span class="highlight">4.3.2.</span> 관리 주기</a></li>
                            </ul>
                        <li style="margin-left: 10px;"><a href="#section4-4" onclick="toggleSection('admin0')"><span class="highlight">4.4.</span> 수영장 배수</a>
                        <li style="margin-left: 10px;"><a href="#section4-5" onclick="toggleSection('admin0')"><span class="highlight">4.5.</span> 수영장 담수</a>
                        <li style="margin-left: 10px;"><a href="#section4-6" onclick="toggleSection('admin0')"><span class="highlight">4.6.</span> 수영장 수온 관리</a>   
                    </ul>     
                </li>
                <li><a href="#section2" onclick="toggleSection('skill5')"><span class="highlight">5.</span> 가스</a>
                </li>
                <li><a href="#section2" onclick="toggleSection('skill6')"><span class="highlight">6.</span> 건축</a>
                </li>
                <li><a href="#section2" onclick="toggleSection('skill7')"><span class="highlight">7.</span> 기타 주요 업무</a>
                </li>
                <li><a href="#section2" onclick="toggleSection('skill8')"><span class="highlight">8.</span> 업체 연락처</a>
                </li>
                                    
            </ul>
        </div>
    
        <!-- 메인 콘텐츠 영역 -->
        <div class="main-content">
            <h6>
                v: 1.04 (2024-11-03)<br>
                creator: 박영규, 박현수
            </h6>
            <h1>가경국민체육센터 기술분야 매뉴얼</h1>
                <script>
                    function toggleTable(tableId, buttonId) {
                        const table = document.getElementById(tableId);
                        const button = document.getElementById(buttonId);
                
                        // Toggle the 'hidden' class on the table to show or hide it
                        table.classList.toggle("hidden");
                
                        // Update the button text based on the table's visibility
                        if (table.classList.contains("hidden")) {
                            button.textContent = buttonId === "toggleUpdateButton" ? "업데이트 현황 [펼치기·접기]" : "시설현황 [펼치기·접기]";
                        } else {
                            button.textContent = buttonId === "toggleUpdateButton" ? "업데이트 현황 [펼치기·접기]" : "시설현황 [펼치기·접기]";
                        }
                    }
                </script>
                <div class="toggle-button" id="toggleUpdateButton" onclick="toggleTable('updateContainer', 'toggleUpdateButton')" style="text-align: center; margin: 20px auto 0 auto; width: fit-content;">
                    업데이트 현황 [펼치기·접기]
                </div>
            <div id="updateContainer" class="hidden">
                <table id="mainTableupdate" style="border-collapse: collapse; width: 100%;">
                    <tr>
                        <th style="width: 5%; text-align: center;">버전</th>
                        <th style="width: 10%;">날짜</th>
                        <th style="width: 85%;">내용</th>
                    </tr>
                    <tr>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">v1.04</td>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">24.11.07</td>
                        <td style="text-align: left; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">
                            - 업데이트 현황 추가 및 구현<br>

                        </td>
                    </tr>
                    <tr>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">v1.05</td>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">24.11.</td>
                        <td style="text-align: left; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">
                            - <br>
                            - <br>
                            - <br>
                        </td>
                    </tr>
                    <tr>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">v1.06</td>
                        <td style="text-align: center; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">24.11.</td>
                        <td style="text-align: left; border-bottom: 1px solid rgba(0, 0, 0, 0.2);">
                            - <br>
                            - <br>
                            - <br>
                    </tr>
                    <tr>
                        <td style="text-align: center;">1.07</td>
                        <td style="text-align: center;">24.11.</td>
                        <td style="text-align: left;">
                            - <br>
                            - <br>
                            - <br>

                    </tr>
                </table>
            </div>  
                
            
            <ul style="list-style-type: none; padding-left: 0;">
                <li class="underline" style="margin-left: 20px;">
                    <h3 id="section1-1" onclick="toggleSection('section1_1_content')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 1.1. 보일러
                    </h3>
                    <!-- 내용 영역 (처음에는 숨겨짐) -->
                    <div id="section1_1_content" class="content hidden" style="margin-left: 20px;">
                        <!-- iframe을 사용해 외부 HTML 파일을 불러오기 -->
                        <iframe src="file:///C:/Users/best/Desktop/공유폴더/2.%20기술분야/21.%20매뉴얼/매뉴얼/매뉴얼/%EA%B0%80%EA%B2%BD%EA%B5%AD%EB%AF%BC%EC%B2%B4%EC%9C%A1%EC%84%BC%ED%84%B0/1.1%20boiler.html" 
                                width="100%" 
                                height="800px" 
                                style="border: none; overflow: hidden; max-width: 100%; box-sizing: border-box;"></iframe>
                    </div>
                </li>
            </ul>
            
            <script>
                function toggleSection(sectionId) {
                    // sectionId에 해당하는 div를 찾음
                    const contentDiv = document.getElementById(sectionId);
                    
                    // 해당 div의 클래스를 토글하여 보이거나 숨김 처리
                    contentDiv.classList.toggle('hidden');
            
                    // 화살표 방향을 바꿈
                    const arrow = contentDiv.previousElementSibling.querySelector('.arrow');
                    if (contentDiv.classList.contains('hidden')) {
                        arrow.classList.remove('expanded');
                        arrow.classList.add('collapsed');
                    } else {
                        arrow.classList.remove('collapsed');
                        arrow.classList.add('expanded');
                    }
                }
            </script>
            
            <style>
                .content.hidden {
                    display: none; /* 내용이 숨겨지도록 설정 */
                }
            
                .arrow {
                    display: inline-block;
                    transition: transform 0.3s ease;
                }
            
                .collapsed {
                    transform: rotate(0deg); /* 오른쪽 화살표 */
                }
            
                .expanded {
                    transform: rotate(90deg); /* 아래쪽 화살표 */
                }
            </style>
            <ul style="list-style-type: none; padding-left: 0;">
                <li class="underline" style="margin-left: 20px;">
                    <h3 id="section1-1" onclick="toggleSection('skill 1.1.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 1.1. 보일러
                    </h3>
                </li>
            </ul>
                    <!-- 펼치기/접기 내용 영역 -->
                        <div id="skill 1.1." class="content hidden" style="margin-left: 20px;">
                            
                            <!-- 상위 테이블 -->
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">세부사항</th> <!-- white-space: nowrap 글씨 길이에 맞춰 너비 자동 조정 -->
                                                    <td style="border: 1px solid #ccc; padding: 10px;">
                                                        <table style="width: 80%; border-collapse: collapse; text-align: center;">
                                                            <tr>
                                                                <th style="border: 1px solid #ccc; text-align: center;">사진</th>
                                                                <td style="border: 1px solid #ccc;">
                                                                    <div class="image-container">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러1.jpg" alt="보일러 사진 1" style="width: 30%; margin: 5px;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러2.jpg" alt="보일러 사진 2"style="width: 30%; margin: 5px;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러3.jpg" alt="보일러 사진 3" style="width: 30%; margin: 5px;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러4.jpg" alt="보일러 사진 4" style="width: 30%; margin: 5px;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러5.jpg" alt="보일러 사진 5" style="width: 30%; margin: 5px;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러6.jpg" alt="보일러 사진 6" style="width: 30%; margin: 5px;">
                                                        </table>
                                                        
                                                        <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">기기명세</th>
                                                        </table>
                                                        <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                            <tr>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">호기</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">형식</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">용량</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">최고사용압력</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">제조사</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">모델번호</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">A/S 연락처</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">비고</th>
                                                            </tr>
                                                            <tr>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1호기</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">관류형 증기</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1.5ton/h</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1Mpa</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">(주)부스타</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">BBS-1500RFX</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1588-3838<br>
                                                                                                                    (주)부스타 콜센터
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                            </tr>
                                                            <tr style="border: 1px solid #ccc; padding: 10px;">
                                                                <td style="border: 1px solid #ccc; padding: 10px;">2호기</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">관류형 증기</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1.5ton/h</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">1Mpa</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">(주)부스타</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">BBS-1500RFX</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">010-3434-9524<br>
                                                                                                                       이기쁨 기사</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                            </tr>
                                                        </table>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none;">
                                                                        <ul style="list-style-type: disc; padding-left: 0px;">
                                                                            <li>보일러 본체</li>
                                                                            <li><span style="color: blue; font-weight: bold;">청관제</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">보일러 청관제는 보일러 내부의 관(배관)과 열교환기에 쌓이는 스케일(석회질)이나 부식을 방지하거나 제거하기 위해 사용하는 화학 첨가제입니다.<br>
                                                                                            보일러 내부를 깨끗하게 유지함으로써 보일러의 열효율을 높이고, 부품 손상을 예방하며, 수명을 연장하는 데 중요한 역할을 합니다.<br>
                                                                                            <br>
                                                                                            보일러 청관제의 주요 기능<br>
                                                                                            <br>
                                                                                            1. 스케일 방지<br>
                                                                                            &nbsp;&nbsp;· 스케일은 물 속의 경도 성분(칼슘, 마그네슘 등)이 고온에서 침전되어 보일러 내부에 축적된 물질입니다.<br>
                                                                                            &nbsp;&nbsp;· 청관제는 스케일 형성을 억제하거나 이미 형성된 스케일을 제거합니다.<br>
                                                                                            <br>
                                                                                            2. 부식 방지<br>
                                                                                            &nbsp;&nbsp;· 보일러 내부는 고온과 고압 상태로 인해 부식이 발생하기 쉬운 환경입니다.<br>
                                                                                            &nbsp;&nbsp;· 청관제는 금속 표면에 얇은 보호막을 형성하여 산소 및 부식성 물질로 인한 손상을 방지합니다.<br>
                                                                                            <br>
                                                                                            3. 열효율 유지<br>
                                                                                            &nbsp;&nbsp;· 스케일이 쌓이면 열전달 효율이 감소하고, 연료 소비량이 증가합니다. 청관제를 사용하면 보일러의 열효율을 유지할 수 있습니다.<br>
                                                                                            <br>
                                                                                            4. 유지 보수 비용 절감<br>                                                                                            
                                                                                            &nbsp;&nbsp;· 보일러 내부가 깨끗하게 유지되면 고장 위험이 줄어들고, 정기적인 점검 및 수리 비용이 절감됩니다.</span>
                                                                                    </span>
                                                                                </sup> 탱크</li>
                                                                            <li><span style="color: blue; font-weight: bold;">연수기</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">보일러 연수기는 보일러에 공급되는 물을 연수(軟水)로 바꾸어 보일러의 성능을 유지하고 수명을 연장시키는 장치입니다.<br>
                                                                                            연수기는 물 속에 포함된 칼슘(Ca), 마그네슘(Mg)과 같은 경도 성분(미네랄)을 제거하거나 줄여주는 역할을 합니다.<br>
                                                                                            <br>
                                                                                            - 주요 기능 및 역할:<br>
                                                                                            <br>
                                                                                            1. 스케일 방지<br>
                                                                                            &nbsp;&nbsp;· 경수(硬水)를 사용할 경우, 물이 가열되면서 칼슘, 마그네슘이 침전되어 **스케일(석회질)**이 보일러 내부에 축적됩니다.<br>
                                                                                            &nbsp;&nbsp;· 연수기는 이 성분을 제거하여 스케일 발생을 방지하고 열교환 효율을 유지합니다.<br>
                                                                                            <br>                                                                                             
                                                                                            2. 보일러 효율 유지<br>
                                                                                            &nbsp;&nbsp;· 스케일이 생기면 열전달이 어려워지고 연료 소모량이 증가합니다. 연수기를 통해 이를 예방하면 연료비를 절감할 수 있습니다.<br>
                                                                                            <br>
                                                                                            3. 부품 손상 방지<br>
                                                                                            &nbsp;&nbsp;· 스케일은 보일러 내부 배관과 열교환기에 손상을 줄 수 있습니다. 연수기를 사용하면 부품 손상 가능성이 줄어듭니다.<br>
                                                                                            <br>
                                                                                            4. 수명 연장<br>
                                                                                            &nbsp;&nbsp;· 연수 처리를 통해 보일러의 과도한 마모와 부식 문제를 줄임으로써, 보일러의 수명을 연장할 수 있습니다.<br>
                                                                                            &nbsp;&nbsp;· 연수기의 작동 원리:<br>
                                                                                            &nbsp;&nbsp;· 연수기는 이온 교환 방식을 사용하여 물 속의 칼슘과 마그네슘 이온을 나트륨(Na) 이온으로 교체합니다. 이를 통해 물을 연수로 바꾸어 보일러에 공급합니다.<br>
                                                                                            &nbsp;&nbsp;· 일정 사용 후에는 연수기에 축적된 경도 성분을 제거하기 위해 재생 작업(소금물 투입 등)이 필요합니다.</span>
                                                                                    </span>
                                                                                </sup></li>
                                                                            <li><span style="color: blue; font-weight: bold;">응축수 탱크</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">보일러 응축수 탱크는 보일러 시스템에서 발생하는 응축수를 수집하고 저장하는 탱크입니다.<br> 
                                                                                            응축수는 보일러에서 연료 연소 후 발생하는 증기의 응축된 물로, 이 물은 보일러 내부의 열교환기나 배관에서 수증기가 냉각되며 형성됩니다.<br>
                                                                                            <br>
                                                                                            1. 보일러 응축수의 특징<br>
                                                                                            &nbsp;온도: 응축수는 일반적으로 80도에서 90도 사이로 고온 상태입니다.<br>
                                                                                            &nbsp;화학 성분: 응축수는 연료의 종류나 보일러 수질에 따라 미세한 화학 성분을 포함할 수 있으며, 이는 보일러 내부에 축적된 스케일 및 부식물질이 포함될 수 있습니다.<br>
                                                                                            <br>
                                                                                            2. 보일러 응축수 탱크의 역할<br>
                                                                                            &nbsp;가. 응축수 회수 및 저장<br>
                                                                                            &nbsp;&nbsp;· 응축수는 연소과정에서 형성된 물로, 이를 회수하여 저장하고 필요 시 다시 보일러 시스템에 공급하여 효율성을 높이는 역할을 합니다.<br>
                                                                                            &nbsp;나. 열 회수<br>
                                                                                            &nbsp;&nbsp;· 응축수는 고온 상태로 보일러 시스템에 유입되므로, 이를 회수하여 재활용함으로써 보일러의 효율성을 높이고 연료 비용을 절감할 수 있습니다.<br>
                                                                                            &nbsp;&nbsp;· 응축수는 일반적으로 열교환기 등을 통해 다른 유체나 공기와 열을 교환하여 에너지를 회수합니다.<br>
                                                                                            &nbsp;다. 수질 관리<br>
                                                                                            &nbsp;&nbsp;· 보일러에서 생성된 응축수에는 미네랄과 화학 물질이 포함될 수 있습니다.<br>
                                                                                            &nbsp;&nbsp;· 이를 적절히 처리하여 다시 사용하는 것이 중요합니다.</span>
                                                                                        </span>
                                                                                </sup></li>    
                                                                            <li>보일러 급수 펌프</li>
                                                                </tr>
                                                            </table>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">운전절차</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none;">
                                                                        <ul style="list-style-type: disc; padding-left: 0px;">
                                                                            <li>보일러 기동 절차</li>
                                                                            <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                                <li>보일러 가동전 <span style="color: blue; font-weight: bold;">가스누설경보기</span>
                                                                                    <sup>
                                                                                        <span class="tooltip" style="color: blue;">[1]
                                                                                            <span class="tooltip-text">보일러 운전 중 발생할 수 있는 가스 누출을 감지하여 안전사고를 예방하는 장치입니다. 주로 산업용 보일러와 상업용 보일러에 설치되며, 가연성 가스가 누출되었을 때 이를 빠르게 감지하고 경고 신호를 통해 사용자를 알립니다.</span>
                                                                                        </span>
                                                                                    </sup>
                                                                                     내 가스누출 경보차단장치의 밸브를 닫힘->열림 설정 변경 및 확인</li>
                                                                                <div style="margin-top: 10px;">※ 가스누설 경보차단장치는 보일러 사용 시 열림 사용 후 닫힘 전환 한다.</div>
                                                                            </ul>
                                                                        </ul>
                                                                    </td>
                                                                    <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                        <!-- 첫 번째 사진, 클릭 시 팝업 -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\가스누설경보기1-1.jpg" 
                                                                             alt="가스 누설 경보기 사진" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </td>
                                                                </tr>
                                                                <tr>
                                                                    <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none;">
                                                                        <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                            <li>가스 사용량 기록을 위해 보일러 뒤에 위치한 유량계의 검침 값 확인 및 기록한다.</li>
                                                                            <li>혹은 자동제어 시스템의 계측기 탭의 가스미터기 값 확인 및 기록한다.</li>
                                                                        </ul>
                                                                    </td>
                                                                    <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러5.jpg" 
                                                                             alt="보일러 사진" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; margin-right: 10px; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\자동제어 계측기1.jpg" 
                                                                             alt="보일러 사진" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </td>
                                                                </tr>
                                                                <tr>
                                                                    <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none;">
                                                                        <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                            <li>자동제어 판넬의 온수가열기 탭에서 온수가열기 순환펌프 환수온도 설정을 20%->60% 변경 적용한다.</li>
                                                                            <li>환수펌프 A or B 작동 확인한다.</li>
                                                                            <li>고압해더 드레인 밸브를 FULL OPEN 한다.(가동 초기시)</li>
                                                                            <li>보일러 기동 전원 ON 후 가스 밸브 열림 상태, 수면계 수위 확인, 기타 초기 상태 확인한다.</li>
                                                                            <li>보일러 컨트롤 판넬의 RUN을 눌러 보일러를 기동 시킨다.</li>
                                                                            <li>가스누설 감지, <span style="color: blue; font-weight: bold;">프리퍼지</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">프리퍼지 (Pre-purge):<br>
                                                                                            보일러가 가동되기 전에 가스를 안전하게 연소할 수 있도록 불필요한 가스나 연료를 배출하는 과정입니다.<br>
                                                                                            연료가 시스템에 공급되기 전에, 공기를 순환시켜 가스 누출이나 불완전 연소를 방지합니다.<br>
                                                                                            이를 통해 연소가 시작될 때 안전하고 효율적인 환경을 만듭니다.</span>
                                                                                    </span>
                                                                                </sup>
                                                                                , 착화, 연소이행 등의 순서로 연소가 이루어진다.</li>
                                                                            <li>
                                                                                점화 및 <span style="color: blue; font-weight: bold;">전배수</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">보일러 내부에 남아 있는 물을 완전히 배출하는 작업으로 보일러를 안전하게 가동하기 위해 필수적이며, 내부의 찌꺼기나 오염물질을 제거하고 보일러의 성능을 유지하는 데 도움이 됩니다.</span>
                                                                                    </span>
                                                                                </sup>
                                                                                작업 실시한다.(가동 초기시)
                                                                            </li>
                                                                            <li>보일러 압력 1.9bar에 도달하면 컨트롤 판넬의 STOP 버튼을 눌러 보일러를 정지 시킨다.</li>
                                                                            <li>보일러가 <span style="color: blue; font-weight: bold;">포스트퍼지</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">포스트퍼지 (Post-purge):<br>
                                                                                            보일러가 가동을 마친 후 연료 공급을 중지한 후, 여전히 남아 있을 수 있는 가스를 제거하기 위한 단계입니다.<br>
                                                                                            이 과정은 보일러 내부에 잔여 가스가 남지 않도록 공기를 순환시켜 안전하게 배출합니다.<br>
                                                                                            포스트퍼지는 보일러가 꺼졌을 때 가스가 잔여하지 않도록 해 사고를 예방하는 역할을 합니다.</span>
                                                                                    </span>
                                                                                </sup>
                                                                                완료 후 연소대기 상태에 도달하면 보일러 전원 버튼을 눌러 OFF 시킨다.</li>
                                                                            <li>수면계 판넬을 열어 아래에 위치한 드레인 밸브를 FULL OPEN 한다.</li>
                                                                            <li>보일러 내부의 물이 잔류 압력으로 배출됨과 동시에 수면계의 수위가 빠르게 내려가며 배수비트로 배출된다.</li>
                                                                            <li>수면계의 수위가 0에 도달하면 열었던 드레인 밸브를 FULL CLOSE 한다.</li>
                                                                            <li>전배수 작업을 실시하면 고압해더 및 배관내 형성되었던 응축수도 배출이 완료됨으로 고압해더 드레인밸브를 FULL CLOSE한다.</li>
                                                                            <li>이전 단계로 돌아가 보일러 기동 전원을 ON 시킨다. 급수 펌프가 기동되며 수위 안정화 상태까지 기다린다.</li>
                                                                            <li>보일러 기동 전원 ON 후 가스 밸브 열림 상태, 수면계 수위 확인, 기타 초기 상태 확인한다.</li>
                                                                            <li>보일러 컨트롤 판넬의 RUN을 눌러 보일러를 기동 시킨다.</li>
                                                                            <li>가스누설 감지, 프리퍼지, 착화, 연소이행 등의 순서로 연소가 이루어진다.</li>
                                                                            <li>연소 운전 진행 후 안정화 상태에 도달하면 보일러 운전절차가 종료된다.</li>
                                                                        </ul>
                                                                    </td>
                                                                    <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                        <div style="display: block; margin-bottom: 10px;">
                                                                            <!-- 첫 번째 줄 (1, 2) -->
                                                                            <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\자동제어 온수가열기1-1.jpg" 
                                                                                alt="자동제어 온수가열기1-1" 
                                                                                style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                                onclick="openPopup(this.src)">
                                                                            <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\고압헤더1-1.jpg" 
                                                                                alt="고압헤더1-1" 
                                                                                style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                                onclick="openPopup(this.src)">
                                                                        </div>
                                                                        <div style="display: block;">
                                                                            <!-- 두 번째 줄 (3, 4) -->
                                                                            <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러2-1.jpg" 
                                                                                alt="보일러 2-1" 
                                                                                style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                                onclick="openPopup(this.src)">
                                                                            <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러2-2.jpg" 
                                                                                alt="보일러2-2" 
                                                                                style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                                onclick="openPopup(this.src)">
                                                                        </div>
                                                                        <div style="display: block;">
                                                                            <!-- 두 번째 줄 (5) -->
                                                                            <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러3-1.jpg" 
                                                                                alt="보일러3-1" 
                                                                                style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                                onclick="openPopup(this.src)">
                                                                        </div>
                                                                    </td>
                                                                </tr>
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        <!-- 팝업 이미지 -->
<div id="popup" onclick="closePopup()">
    <span>&times;</span>
    <img id="popup-img" src="" alt="보일러 사진">
</div>
                        </div>
                        <ul style="list-style-type: none; padding-left: 0;">
                            <li class="underline" style="margin-left: 20px;">
                                <h3 id="section1-2" onclick="toggleSection('skill 1.2.')" style="cursor: pointer;">
                                    <span class="arrow collapsed">></span> 1.2. 수영장 제어설비
                                </h3>
                            </li>
                        </ul>
                    
                    <!-- 펼치기/접기 내용 영역 -->
                    <div id="skill 1.2." class="content hidden" style="margin-left: 20px;">
                            
                        <!-- 상위 테이블 -->
                        <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                            <tr>
                                
                                <td>
                                    <div id="detailTable0" class="details">
                                        <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                            <tr>
                                                <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">세부사항</th> <!-- white-space: nowrap 글씨 길이에 맞춰 너비 자동 조정 -->
                                                <td style="border: 1px solid #ccc; padding: 10px;">
                                                    <table style="width: 80%; border-collapse: collapse; text-align: center;">
                                                        <tr>
                                                            <th style="border: 1px solid #ccc; text-align: center;">사진</th>
                                                            <td style="border: 1px solid #ccc;">
                                                                <div class="image-container">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장 수질관리1.jpg" alt="수영장 수질관리1" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장 순환펌프1.jpg" alt="수영장 수질관리2"style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\여과기1.jpg" alt="수영장 수질관리3" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\열교환기1.jpg" alt="수영장 수질관리4" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\밸런스탱크1.jpg" alt="수영장 수질관리5" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\약품관리1.jpg" alt="수영장 수질관리6" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\약품관리2.jpg" alt="수영장 수질관리7" style="width: 30%; margin: 5px;">
                                                                <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\약품관리3.jpg" alt="수영장 수질관리8" style="width: 30%; margin: 5px;">
                                                    </table>
                                                    
                                                    <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">기기명세</th>
                                                    </table>
                                                    <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                        <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">명칭</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">형식</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">용량</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">대수</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">제조사</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">모델번호</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">A/S 연락처</th>
                                                        <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap; font-weight: bold;">비고</th>
                                                        </tr>
                                                        <tr>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">수질관리 제어반</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">터치패널</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">1</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)코리아 이피디</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">010-5618-1341<br>
                                                                                                                이재빈 대리
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">여과기</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">횡형 압력식<br>
                                                                                                                    수동, 자동, 반자동</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">138t/h</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">3</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)코리아이피디</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">010-7642-1018<br>
                                                                                                                                      이두성 차장</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">수영장 순환펌프</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">인라인 펌프</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">18.5kw(25HP), 2.3㎥/min</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">2</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">하이젠모터<br>
                                                                                                                ㈜대영파워펌프</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">P25HU1FIL-DY</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)바로이엔씨<br>
                                                                                                                010-4067-8270<br>
                                                                                                                한상용 설비소장</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">열교환기</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">판형</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">400,000kcal/h</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">1</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">태봉산업기술㈜</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">PI2320881</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)바로이엔씨<br>
                                                                                                                010-4067-8270<br>
                                                                                                                한상용 설비소장</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">밸런싱탱크</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">SMC</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">36Ton</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">1</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">관급</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">차염발생장치</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">오픈셀방식</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">6kg/day (일일생산량)</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">1</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)하이클로</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">010-3208-9695<br>
                                                                                                                남진수 팀장
                                                            </td>
                                                            <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                        </tr>
                                                        <tr style="border: 1px solid #ccc; padding: 10px;">
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">수질자동측정장치</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">1</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">(주)코리아이피디</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">-</td>
                                                            <td style="border: 1px solid #ccc; padding: 10px; font-weight: normal;">010-5618-1341<br>
                                                                                                                이재빈 대리
                                                            </td>
                                                            <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                        </tr>
                                                    </table>
                                                </td>
                                            </tr>
                                            <tr>
                                                <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                    <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                        <table style="width: 100%; border-collapse: collapse;">
                                                            <tr>
                                                                <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none; font-weight: normal;">
                                                                    <ul style="list-style-type: disc; padding-left: 0px;">
                                                                        <li>수질관리 제어반</li>
                                                                        <li><span style="color: blue; font-weight: bold;">여과기</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장 여과기의 주요 목적은 수영장의 물을 깨끗하고 안전하게 유지하는 것입니다.<br>
                                                                                        이를 통해 수영자들에게 쾌적한 환경을 제공하고, 물 관리 비용을 절감하며, 수질 관련 문제를 예방할 수 있습니다.<br>
                                                                                        <br>
                                                                                        &nbsp;여과기의 역할<br>
                                                                                        <br>
                                                                                        &nbsp;&nbsp;· 물 속의 먼지, 모래, 머리카락, 유기물 등 불순물을 걸러냅니다.<br>
                                                                                        &nbsp;&nbsp;· 수질의 탁도를 낮추고 깨끗한 물을 제공합니다.<br>
                                                                                        &nbsp;&nbsp;· 살균제를 효율적으로 작용하게 만들어 수질 유지 비용을 절감합니다.<br>
                                                                                </span>
                                                                            </sup></li>
                                                                        <li><span style="color: blue; font-weight: bold;">순환펌프</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장 순환펌프는 수영장의 물을 여과 시스템과 살균 시스템으로 순환시키는 핵심 장비입니다.<br>
                                                                                        이 장치는 물이 정체되지 않고 지속적으로 순환되도록 하여 수질을 깨끗하게 유지하고, 균일한 온도와 화학 성분 분포를 제공합니다.<br>
                                                                                        <br>
                                                                                        수영장 순환펌프의 역할<br>
                                                                                        <br>

                                                                                        &nbsp;1. 물 순환<br>
                                                                                        &nbsp;&nbsp;· 수영장의 물을 여과기로 보내 불순물을 제거하고 깨끗한 물이 다시 수영장으로 돌아오도록 합니다.<br>
                                                                                        &nbsp;&nbsp;· 정체된 물이 없도록 하여 균일한 수질 유지.<br>
                                                                                        &nbsp;2. 화학물질 혼합<br>
                                                                                        &nbsp;&nbsp;· 살균제(염소) 및 pH 조절제와 같은 화학 물질을 균일하게 분산시켜 수질을 안정적으로 유지.<br>
                                                                                        &nbsp;3. 온도 균일화<br>
                                                                                        &nbsp;&nbsp;· 히터에서 가열된 물을 전체 수영장으로 순환시켜 균일한 온도를 유지.<br>
                                                                                        &nbsp;4. 불순물 제거 지원<br>
                                                                                        &nbsp;&nbsp;· 표면에 떠다니는 쓰레기나 이물질이 스키머와 배수구로 흡입되어 여과기로 보내지도록 도와줍니다.</span>
                                                                            </sup></li>
                                                                            <li><span style="color: blue; font-weight: bold;">집모기</span>
                                                                                <sup>
                                                                                    <span class="tooltip" style="color: blue;">[1]
                                                                                        <span class="tooltip-text">이물질 관리

                                                                                            물과 함께 들어오는 큰 이물질(머리카락, 낙엽 등)을 막아주는 거름망(스크린)이 설치되어 있습니다.
                                                                                            이는 순환펌프와 여과 장치의 손상을 방지합니다.<br>
                                                                                            <br>
                                                                                            수영장 열교환기의 주요 역할<br>
                                                                                            <br>
                                                                                            &nbsp;1. 물 가열<br>
                                                                                            &nbsp;&nbsp;· 찬 수영장 물에 열을 전달하여 적정 온도로 가열합니다.<br>
                                                                                            &nbsp;&nbsp;· 겨울철 또는 온도가 낮은 날씨에 사용량 증가.<br>
                                                                                            &nbsp;2. 물 냉각<br>
                                                                                            &nbsp;&nbsp;· 여름철이나 고온 환경에서 과열된 물을 냉각시켜 쾌적한 온도로 유지합니다.<br>
                                                                                            &nbsp;3. 온도 유지<br>
                                                                                            &nbsp;&nbsp;· 외부 환경 온도의 변화에도 불구하고 일정한 수영장 물 온도를 유지.<br>
                                                                                            &nbsp;4. 에너지 효율성 향상<br>
                                                                                            &nbsp;&nbsp;· 보일러나 히트펌프와 연계하여 에너지 소비를 최적화.
                                                                                        </span>
                                                                                </sup></li>   
                                                                            <li><span style="color: blue; font-weight: bold;">열교환기</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장 열교환기는 수영장 물의 온도를 일정하게 유지하기 위해 사용하는 장치로, 외부 열원(온수, 보일러, 히트펌프 등)을 이용해 수영장 물을 가열하거나 냉각합니다.<br>
                                                                                        이를 통해 쾌적한 수영 환경을 제공하며, 특히 실내 수영장이나 사계절 운영 수영장에서 중요한 역할을 합니다.<br>
                                                                                        <br>
                                                                                        수영장 열교환기의 주요 역할<br>
                                                                                        <br>
                                                                                        &nbsp;1. 물 가열<br>
                                                                                        &nbsp;&nbsp;· 찬 수영장 물에 열을 전달하여 적정 온도로 가열합니다.<br>
                                                                                        &nbsp;&nbsp;· 겨울철 또는 온도가 낮은 날씨에 사용량 증가.<br>
                                                                                        &nbsp;2. 물 냉각<br>
                                                                                        &nbsp;&nbsp;· 여름철이나 고온 환경에서 과열된 물을 냉각시켜 쾌적한 온도로 유지합니다.<br>
                                                                                        &nbsp;3. 온도 유지<br>
                                                                                        &nbsp;&nbsp;· 외부 환경 온도의 변화에도 불구하고 일정한 수영장 물 온도를 유지.<br>
                                                                                        &nbsp;4. 에너지 효율성 향상<br>
                                                                                        &nbsp;&nbsp;· 보일러나 히트펌프와 연계하여 에너지 소비를 최적화.
                                                                                    </span>
                                                                            </sup></li> 
                                                                                 
                                                                        <li>밸런싱 탱크</li>
                                                                        <li><span style="color: blue; font-weight: bold;">차염발생장치</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장에서 사용하는 차염발생장치(차아염소산나트륨 발생기)는 물의 소독 및 살균을 위해 차아염소산나트륨(일반적으로 '차염'이라 불림)을 생산하는 장치입니다.<br>
                                                                                        이 장치는 물의 위생을 유지하고 수질 관리를 용이하게 하는 데 중요한 역할을 합니다.<br>
                                                                                        <br>
                                                                                        차염발생장치의 주요 기능<br>
                                                                                        <br>
                                                                                        &nbsp;1. 소독제 생산<br>
                                                                                        &nbsp;&nbsp;· 소금(NaCl)을 전기 분해하여 차아염소산나트륨(NaClO)을 생성.<br>
                                                                                        &nbsp;&nbsp;· 생성된 NaClO는 물 속의 유기물, 박테리아, 바이러스를 제거.<br>
                                                                                        &nbsp;2. 안전한 수질 관리<br>
                                                                                        &nbsp;&nbsp;· 수영장의 pH와 잔류염소 농도를 일정하게 유지.<br>
                                                                                        &nbsp;&nbsp;· 수질 관리를 위한 화학약품 사용량 감소.<br>
                                                                                        &nbsp;3. 효율적인 운용<br>
                                                                                        &nbsp;&nbsp;· 즉석 생산으로 화학약품 저장의 필요성을 줄임.<br>
                                                                                        &nbsp;&nbsp;· 비용 절감 및 장기적으로 더 안전한 운영 환경 제공.<br>
                                                                                    </span>
                                                                            </sup></li> 
                                                                        <li><span style="color: blue; font-weight: bold;">차염 주입펌프</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장 차염 주입펌프는 수질 소독을 위해 차아염소산나트륨(차염)을 일정량으로 자동 주입하는 장비입니다.<br>
                                                                                        이 장치는 수영장의 위생을 유지하고 물 속의 세균, 바이러스 등을 효과적으로 제거하는 데 필수적입니다.<br>
                                                                                        <br>
                                                                                        차염 주입펌프의 주요 역할<br>
                                                                                        <br>
                                                                                        &nbsp;1. 소독제 주입<br>
                                                                                        &nbsp;&nbsp;· 수영장 물에 차염(소독제)을 정확한 농도로 주입.<br>
                                                                                        &nbsp;&nbsp;· 잔류 염소 농도를 일정하게 유지(법적 기준 농도: 0.4~1ppm).<br>
                                                                                        &nbsp;2. 유의사항<br>
                                                                                        &nbsp;&nbsp;· 적정 농도 유지: 차염 농도가 너무 높으면 사용자 불편을 초래할 수 있음.<br>
                                                                                        &nbsp;&nbsp;· 수질 모니터링: 수영장 물의 pH와 염소 농도를 주기적으로 확인.<br>
                                                                                    </span>
                                                                        <li><span style="color: blue; font-weight: bold;">pH 주입펌프</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장에서 사용하는 **pH 주입펌프(pH 조절 펌프)**는 수질 관리를 위해 수영장의 물 pH를 일정하게 유지하는 장치입니다.<br>
                                                                                        이 장치는 수영장 물의 알칼리성이나 산성을 조절하여 소독제의 효과를 극대화하고 사용자에게 쾌적한 환경을 제공합니다.<br>
                                                                                        <br>
                                                                                        pH 주입펌프의 주요 역할<br>
                                                                                        <br>
                                                                                        &nbsp;1. pH 조절<br>
                                                                                        &nbsp;&nbsp;· 수영장 물의 pH가 높으면(알칼리성) 산성 물질을 주입.<br>
                                                                                        &nbsp;&nbsp;· pH가 낮으면(산성) 알칼리성 물질을 주입.<br>
                                                                                        &nbsp;&nbsp;· 일반적인 수영장의 적정 pH 범위: 7.2 ~ 7.6.<br>
                                                                                        &nbsp;2. 소독제 효율 최적화<br>
                                                                                        &nbsp;&nbsp;· pH가 너무 높거나 낮으면 소독제(차염 등)의 살균 효과 감소.<br>
                                                                                        &nbsp;&nbsp;· 적정 pH 유지로 수질 관리 효율 상승.<br>
                                                                                        &nbsp;3. 사용자 안전 및 편안함<br>
                                                                                        &nbsp;&nbsp;· 적정 pH는 피부 자극 최소화 및 장비 부식 방지.<br>
                                                                                    </span>
                                                                        <li><span style="color: blue; font-weight: bold;">응집제 주입펌프</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">수영장 응집제 주입펌프는 물 속의 미세 입자와 부유물을 효과적으로 제거하기 위해 응집제를 주입하는 장치입니다.<br>
                                                                                        이 펌프는 수질을 깨끗하게 유지하며, 특히 수영장의 탁도를 개선하고 필터링 시스템의 효율성을 높이는 데 중요한 역할을 합니다.<br>
                                                                                        <br>
                                                                                        응집제 주입펌프의 역할<br>
                                                                                        <br>
                                                                                        &nbsp;1. 미세 입자 제거<br>
                                                                                        &nbsp;&nbsp;· 물 속의 작은 입자(오염물질, 유기물 등)를 응집제를 통해 뭉치게 함..<br>
                                                                                        &nbsp;&nbsp;· 입자가 뭉쳐 커져 수영장 아래로 가라앉은 덩어리(플록, floc)는 수중청소기로 쉽게 제거.<br>
                                                                                        &nbsp;2. 탁도 개선<br>
                                                                                        &nbsp;&nbsp;· 응집 작용으로 물을 맑고 깨끗하게 유지..<br>
                                                                                        &nbsp;&nbsp;· 시각적으로 더 깨끗한 수질 제공.<br>
                                                                                    </span>
                                                            </tr>
                                                        </table>
                                            </tr>
                                            <tr>
                                                <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">운전절차</th>
                                                <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                    <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                        <table style="width: 100%; border-collapse: collapse;">
                                                            <tr>
                                                                <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none; font-weight: normal;">
                                                                    <ul style="list-style-type: disc; padding-left: 0px;">
                                                                        <li>역세 운전 절차</li>
                                                                        <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                            <li>역세 운전 전 <span style="color: blue; font-weight: bold;">수영장 수 순환 설비의 밸브 상태</span>를 확인 한다.<br> 
                                                                                (순환펌프 흡입 측, 토출 측, 여과기 흡입 측, 토출 측 드레인 측 등의 밸브 개방 상태 확인)</li>
                                                                            ※ 펌프 흡입·토출, 여과기 흡입·토출, 드레인 등의 밸브가 닫힘상태로 운전시 설비 혹은 배관에 대미지를 줄수 있다.</div>
                                                                            <li><span style="color: blue; font-weight: bold;">밸런스 탱크 수위를 확인</span>(수영장 컨트롤 판넬 수위 및 밸런스 탱크 실제 수위)를 확인 한다.</li>
                                                                            ※ 역세운전 시 밸런스 탱크 내 수위로 역세운전이 이루어지며 수위가 저수위에 도달시 순환펌프가 정지된다.</div>
                                                                            <li>밸런스 탱크 내 수위가 50~60% 상태일 경우 밸런스 탱크 상수도 보충을 실시한다.(저수위 펌프 정지 대비)약 80%정도</li>
                                                                            <li>밸런스 탱크 수위 보충 절차(자동운전(AUTO) 상태)</li>
                                                                            <div style="margin-top: 5px;">- 밸런스 탱크 중수위 50% 클릭 후 현재 수위보다 높게 설정한다.</div>
                                                                            <div style="margin-top: 5px;">- 중수위 변경시 상수도 시수밸브 가동 조건 성립되어 시수밸브가 열린다.</div>
                                                                            <div style="margin-top: 5px;">- 고수위는 시수밸브 정지 조건으로 고수위를 70%->80%으로 변경하여 추가 보충한다.</div>
                                                                            <div style="margin-top: 5px;">※ 중수위/고수위 설정 값은 역세 운전 종료 후 기본 설정값으로 복원시킨다. </div>
                                                                            <li style="margin-top: 5px;">가압펌프 가동상태 확인한다.</li>
                                                                            ※ 가압펌프는 여과기의 솔밸브 작동 역활을 한다. 가압펌프가 정지되어 있으면 역세 혹은 여과기 작동 밸브가 동작하지 않는다.</div>
                                                                            

                                                                        </ul>
                                                                    </ul>
                                                                </td>
                                                                <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                    <div style="display: block; margin-bottom: 10px;">
                                                                        <!-- 첫 번째 줄 (1, 2) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장 순환펌프1-1.jpg" 
                                                                             alt="수영장 순환펌프1-1" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\여과기2-1.jpg" 
                                                                             alt="여과기2-1" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                                    <div style="display: block;">
                                                                        <!-- 두 번째 줄 (3, 4) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장3-1.jpg" 
                                                                             alt="수영장3-1" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장4-1.jpg" 
                                                                             alt="수영장4-1" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                                    <div style="display: block;">
                                                                        <!-- 두 번째 줄 (5) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장3-2.jpg" 
                                                                             alt="수영장3-2" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                             <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\수영장3-3.jpg" 
                                                                             alt="수영장3-3" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                            </tr>
                                                            <tr>
                                                                <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none; font-weight: normal;">
                                                                    <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                        <li>여과기 역세 운전 조건이 준비 되었으면 역세예약(자동역세) 혹은 수동역세를 클릭하여 역세를 진행한다.</li>
                                                                        <li>역세예약(자동역세) 운전 절차</li>
                                                                            <div style="margin-top: 5px;">- 역세예약과 강제역세시작 빈공간을 클릭하면 역세 설정 화면으로 전환된다.</div>
                                                                            <div style="margin-top: 5px;">- 주간역세(월~일 까지 요일별 설정)와 매일역세(매일반복 설정) 운전 주기를 설정을 할수 있다.</div>
                                                                            <div style="margin-top: 5px;">- 보통 주간역세로 실시하며 해당 요일에 3회 까지 적용 운전할수 있다.</div>
                                                                            <div style="margin-top: 5px;">- 해당 요일 시간을 컨트롤 화면 우측 상단의 시간보다 뒤로 설정하면 해당시간 도래시 역세가 시작된다.</div>
                                                                            <div style="margin-top: 5px;">- 여과기 1번, 2번, 3번 순서로 진행되며 5분 역세 후 2분 대기 순서로 진행된다. </div>
                                                                            <div style="margin-top: 5px;">- 역세 가동시간과 대기시간도 변경이 가능하다.</div>
                                                                            <div style="margin-top: 5px;">- 역세 설정을 마췄으면 메인화면으로 돌아온다.</div>
                                                                            <div style="margin-top: 5px;">- 메인 컨트롤 화면의 역세예약을 클릭하면 활성화가 되며 역세예약 운전이 시작된다.</div>
                                                                            <div style="margin-top: 5px;">- 가압펌프가 작동하며 여과기 1번부터 솔벨브 작동과 함께 역세가 시작된다.</div> 
                                                                            <div style="margin-top: 5px;">- 역세가 시작되면 자리를 이탈하지 않고 역세과정을 지켜보며 여과기 밸브의 정상 작동상태와 밸런스탱크 수위를 지속 관찰한다.</div>
                                                                            <div style="margin-top: 5px;">※ 문제 발생시 역세 정지 혹은 응급상황시는 여과기 순환펌프까지 정지한다.</div>
                                                                            <div style="margin-top: 5px;">- 여과기 3번까지 역세가 완료되면 역세 운전이 종료된다.</div>
                                                                            <div style="margin-top: 5px;">- 앞서 밸런스 탱크 수위변경 값을 초기 설정값으로 변경한다.</div>
                                                                            
                                                                    </ul>
                                                                </td>
                                                                <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러5.jpg" 
                                                                         alt="보일러 사진" 
                                                                         style="max-width: 180px; height: 150px; display: inline-block; margin-right: 10px; cursor: pointer;" 
                                                                         onclick="openPopup(this.src)">
                                                                    <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\자동제어 계측기1.jpg" 
                                                                         alt="보일러 사진" 
                                                                         style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                         onclick="openPopup(this.src)">
                                                                </td>
                                                            </tr>
                                                            <tr>
                                                                <td style="vertical-align: top; padding: 10px; width: 70%; border-right: none;">
                                                                    <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                        <li>자동제어 판넬의 온수가열기 탭에서 온수가열기 순환펌프 환수온도 설정을 20%->60% 변경 적용한다.</li>
                                                                        <li>환수펌프 A or B 작동 확인한다.</li>
                                                                        <li>고압해더 드레인 밸브를 FULL OPEN 한다.(가동 초기시)</li>
                                                                        <li>보일러 기동 전원 ON 후 가스 밸브 열림 상태, 수면계 수위 확인, 기타 초기 상태 확인한다.</li>
                                                                        <li>보일러 컨트롤 판넬의 RUN을 눌러 보일러를 기동 시킨다.</li>
                                                                        <li>가스누설 감지, <span style="color: blue; font-weight: bold;">프리퍼지</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">프리퍼지 (Pre-purge):<br>
                                                                                        보일러가 가동되기 전에 가스를 안전하게 연소할 수 있도록 불필요한 가스나 연료를 배출하는 과정입니다.<br>
                                                                                        연료가 시스템에 공급되기 전에, 공기를 순환시켜 가스 누출이나 불완전 연소를 방지합니다.<br>
                                                                                        이를 통해 연소가 시작될 때 안전하고 효율적인 환경을 만듭니다.</span>
                                                                                </span>
                                                                            </sup>
                                                                            , 착화, 연소이행 등의 순서로 연소가 이루어진다.</li>
                                                                        <li>
                                                                            점화 및 <span style="color: blue; font-weight: bold;">전배수</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">보일러 내부에 남아 있는 물을 완전히 배출하는 작업으로 보일러를 안전하게 가동하기 위해 필수적이며, 내부의 찌꺼기나 오염물질을 제거하고 보일러의 성능을 유지하는 데 도움이 됩니다.</span>
                                                                                </span>
                                                                            </sup>
                                                                            작업 실시한다.(가동 초기시)
                                                                        </li>
                                                                        <li>보일러 압력 1.9bar에 도달하면 컨트롤 판넬의 STOP 버튼을 눌러 보일러를 정지 시킨다.</li>
                                                                        <li>보일러가 <span style="color: blue; font-weight: bold;">포스트퍼지</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">포스트퍼지 (Post-purge):<br>
                                                                                        보일러가 가동을 마친 후 연료 공급을 중지한 후, 여전히 남아 있을 수 있는 가스를 제거하기 위한 단계입니다.<br>
                                                                                        이 과정은 보일러 내부에 잔여 가스가 남지 않도록 공기를 순환시켜 안전하게 배출합니다.<br>
                                                                                        포스트퍼지는 보일러가 꺼졌을 때 가스가 잔여하지 않도록 해 사고를 예방하는 역할을 합니다.</span>
                                                                                </span>
                                                                            </sup>
                                                                            완료 후 연소대기 상태에 도달하면 보일러 전원 버튼을 눌러 OFF 시킨다.</li>
                                                                        <li>수면계 판넬을 열어 아래에 위치한 드레인 밸브를 FULL OPEN 한다.</li>
                                                                        <li>보일러 내부의 물이 잔류 압력으로 배출됨과 동시에 수면계의 수위가 빠르게 내려가며 배수비트로 배출된다.</li>
                                                                        <li>수면계의 수위가 0에 도달하면 열었던 드레인 밸브를 FULL CLOSE 한다.</li>
                                                                        <li>전배수 작업을 실시하면 고압해더 및 배관내 형성되었던 응축수도 배출이 완료됨으로 고압해더 드레인밸브를 FULL CLOSE한다.</li>
                                                                        <li>이전 단계로 돌아가 보일러 기동 전원을 ON 시킨다. 급수 펌프가 기동되며 수위 안정화 상태까지 기다린다.</li>
                                                                        <li>보일러 기동 전원 ON 후 가스 밸브 열림 상태, 수면계 수위 확인, 기타 초기 상태 확인한다.</li>
                                                                        <li>보일러 컨트롤 판넬의 RUN을 눌러 보일러를 기동 시킨다.</li>
                                                                        <li>가스누설 감지, 프리퍼지, 착화, 연소이행 등의 순서로 연소가 이루어진다.</li>
                                                                        <li>연소 운전 진행 후 안정화 상태에 도달하면 보일러 운전절차가 종료된다.</li>
                                                                    </ul>
                                                                </td>
                                                                <td style="vertical-align: top; padding: 10px; width: 30%; text-align: right; border-left: none;">
                                                                    <div style="display: block; margin-bottom: 10px;">
                                                                        <!-- 첫 번째 줄 (1, 2) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\자동제어 온수가열기1-1.jpg" 
                                                                             alt="자동제어 온수가열기1-1" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\고압헤더1-1.jpg" 
                                                                             alt="고압헤더1-1" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                                    <div style="display: block;">
                                                                        <!-- 두 번째 줄 (3, 4) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러2-1.jpg" 
                                                                             alt="보일러 2-1" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러2-2.jpg" 
                                                                             alt="보일러2-2" 
                                                                             style="max-width: 180px; height: 150px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                                    <div style="display: block;">
                                                                        <!-- 두 번째 줄 (5) -->
                                                                        <img src="C:\Users\best\Desktop\공유폴더\2. 기술분야\21. 매뉴얼\매뉴얼\매뉴얼\가경국민체육센터\사진\보일러3-1.jpg" 
                                                                             alt="보일러3-1" 
                                                                             style="max-width: 180px; height: 150px; margin-right: 10px; display: inline-block; cursor: pointer;" 
                                                                             onclick="openPopup(this.src)">
                                                                    </div>
                                                                </td>
                                                            </tr>
                                                            </tr>
                                                        </table>
                                                    </ul>
                                                </td>
                                            </tr>
                                            
                                        </table>
                                    </div>
                                </td>
                            </tr>
                        </table>
                        <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                    <!-- 팝업 이미지 -->
                    

                    <h3 id="section1-3" onclick="toggleSection('skill 1.3.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 1.3. 온수가열기
                    </h3>

                        <div id="skill 1.3." class="content hidden" style="margin-left: 20px;">
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        </div>

                    <h3 id="section1-4" onclick="toggleSection('skill 1.4.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 1.4. 공조기
                    </h3>

                        <div id="skill 1.4." class="content hidden" style="margin-left: 20px;">
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        </div>
                
                </li>
            </ul>

            <h2 id="section2" onclick="toggleSection('skill2')">2. 전기</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                    <h3 id="section2-1" onclick="toggleSection('skill 2.1.')" style="cursor: pointer;">
                    <span class="arrow collapsed">></span> 2.1. 정전
                    </h3>
    
                    <!-- 펼치기/접기 내용 영역 -->
                        <div id="skill 2.1." class="content hidden" style="margin-left: 20px;">
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        </div>

                    <h3 id="section2-2" onclick="toggleSection('skill 2.2.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 2.2. 복전
                    </h3>

                        <div id="skill 2.2." class="content hidden" style="margin-left: 20px;">
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        </div>

                    <h3 id="section2-3" onclick="toggleSection('skill 2.3.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 2.3. 기타
                    </h3>

                        <div id="skill 1.3." class="content hidden" style="margin-left: 20px;">
                            <!-- 원하는 추가 콘텐츠를 여기에 추가 -->
                        </div>
                
                </li>
            </ul>

            <h2 id="section3" onclick="toggleSection('skill3')">3. 소방</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                    <h3 id="section3-1" onclick="toggleSection('skill 3.1.')" style="cursor: pointer;">
                    <span class="arrow collapsed">></span> 3.1. 화재감지기 작동 및 화재발생 대응
                    </h3>
    
                    <!-- 펼치기/접기 내용 영역 -->
                        <div id="skill 3.1." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 100%; border-collapse: collapse; text-align: center;">

                                <tr>
                                          <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                            
                                        </ul>
                                    </td>
                                </tr>
                                <tr>
                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">화재발생 대응</th>
                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                            <li>화재경보가 발생하였을 경우 4층에 있는 P형 복합 수신기로 이동</li>
                                            <li>지구경종정지,주음양정지,스위치잠금,시각경보,비상방송,사이렌,확인음향 순으로 활성화</li>
                                            <li>화재경보기가 울리는 장소 확인</li>
                                            <li>화재경보기가 오류일 경우 복구 선택</li>
                                            <li>실제 화재일 경우 역순으로 비활성화 후 화재 방송</li>
                                        </ul>
                                    </td>
                                </tr>
                                
                            </table>
                        </div>
                </li>
            </ul>

            <h2 id="section4" onclick="toggleSection('skill4')">4. 수질</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                    <h3 id="section4-1" onclick="toggleSection('skill 4.1.')" style="cursor: pointer;">
                    <span class="arrow collapsed">></span> 4.1. 수영장 수질 자동측정 장치
                    </h3>
    
                    <!-- 펼치기/접기 내용 영역 -->
                        <div id="skill 4.1." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">세부사항</th> <!-- white-space: nowrap 글씨 길이에 맞춰 너비 자동 조정 -->
                                                    <td style="border: 1px solid #ccc; padding: 10px;">

                                                        <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">기기명세</th>
                                                        </table>
                                                        <table style="width: 100%; border-collapse: collapse; margin: 0; text-align: center;">
                                                            <tr>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">종류</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">형식</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">제조사</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">모델번호</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">A/S 연락처</th>
                                                            <th style="border: 1px solid #ccc; padding: 10px; text-align: center; white-space: nowrap;">비고</th>
                                                            </tr>
                                                            <tr>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">염소측정장치</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">프로미넌트</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                            </tr>
                                                            <tr style="border: 1px solid #ccc; padding: 10px;">
                                                                <td style="border: 1px solid #ccc; padding: 10px;">PH측정장치</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;">프로미넌트</td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                                <td style="border: 1px solid #ccc; padding: 10px;"></td>
                                                            </tr>
                                                        </table>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                <!-- 내용 -->
                                                                </tr>
                                                            </table>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">설정방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <!-- 내용 -->
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>

                    <h3 id="section4-2" onclick="toggleSection('skill 4.2.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 4.2. 수영장 염소 측정
                    </h3>

                        <div id="skill 4.2." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">

                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <li>수영장의 염소 수치는 물의 위생 상태를 유지하고 박테리아와 유기물을 제거하기 위해 매우 중요한 요소입니다. 염소 수치는 수영장 물의 살균 효과를 보장하면서도 사용자에게 안전해야 합니다. 일반적으로 다음과 같은 기준이 권장됩니다:</li>
                                                                    <li>염소 적정 범위</li>
                                                                        <ul style="list-style-type: circle; padding-left: 20px; margin-top: 10px;">
                                                                            <li><span style="color: blue; font-weight: bold;">자유염소</span>: 0.4 ~ 1.0 ppm</li>
                                                                            <li><span style="color: blue; font-weight: bold;">결함염소</span>: 0.5 ppm 이하</li>
                                                                        </ul>
                                                                    <li>하루에 3번 측정을 하여 적정값 유지</li>
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">측정방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">비색계측정</th>
                                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                            <li>비색계 용기에 샘플 물을 1/3 정도 채워 주세요.</li>
                                                                            <li>물에 약품을 6방울 정도 떨어뜨립니다. </li>
                                                                            <li>측정기기를 빛이 잘 보이는 곳으로 향하게 하여 랜즈를 통하여 측정합니다.</li>
                                                                            <li>옆에 있는 샘플 색을 비교를 하며 염소 측정을 합니다.</li>
                                                                        </ul>
                                                                    </td>
                                                                </tr>
                                                                <tr>
                                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">가루약측정</th>
                                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                            <li>용기에 10mL를 채취합니다.</li>   
                                                                            <li>측정기기의 전원을 켠 뒤, 측정 방법을 선택합니다: [Free Cl (powder)] 또는 [Total Cl (powder)]</li>
                                                                            <li>용기를 측정기에 넣고 Zero 값을 설정합니다.</li>
                                                                            <li>용기에 시약을 투입한 후, 가루가 완전히 녹을 때까지 흔듭니다.</li>
                                                                            <li>용기를 다시 측정기에 넣고 측정합니다.</li>
                                                                        </ul>
                                                                    </td>
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>

                    <h3 id="section4-3" onclick="toggleSection('skill 4.3.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 4.3. 수영장 약품관리
                    </h3>

                        <div id="skill 4.3." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">

                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <li><span style="color: blue; font-weight: bold;">PH감소제</span>
                                                                        <sup>
                                                                            <span class="tooltip" style="color: blue;">[1]
                                                                                <span class="tooltip-text">pH 감소제는 수영장 물의 pH가 높은 경우 이를 낮춰 적정 범위(7.2~7.8)로 조정하는 데 사용되는 약품입니다.<br>
                                                                                    
                                                                            </span>
                                                                        </sup></li>

                                                                    <li><span style="color: blue; font-weight: bold;">응집제(매직풀900)</span>
                                                                        <sup>
                                                                            <span class="tooltip" style="color: blue;">[1]
                                                                                <span class="tooltip-text">응집제는 수영장 물 속의 미세한 입자와 불순물을 뭉쳐 더 큰 덩어리(플록, Floc)를 형성하도록 돕는 화학 물질입니다. 이 과정으로 물속에 떠다니는 불순물을 제거해 물을 맑고 깨끗하게 유지합니다.<br>
                                                                                </span>
                                                                        </sup></li>

                                                                        <li><span style="color: blue; font-weight: bold;">매직쇼크</span>
                                                                            <sup>
                                                                                <span class="tooltip" style="color: blue;">[1]
                                                                                    <span class="tooltip-text">매직쇼크는 수영장 물의 상태를 급격히 개선하기 위해 사용하는 강력한 산화제입니다. 주로 수영장 물 속에 축적된 유기물, 결합 염소, 조류 등을 제거하고 염소의 소독 효과를 회복시키는 데 사용됩니다.<br>
                                                                                        <br>
                                                                                        매직쇼크의 주요 기능<br>
                                                                                        <br>
                                                                                        &nbsp;1. 탁도개선<br>
                                                                                        &nbsp;&nbsp;· 물속 불순물 산화 및 제거로 맑은 물 유지.<br>
                                                                                        &nbsp;2. 염소 수치 균형<br>
                                                                                        &nbsp;&nbsp;· 결합 염소 감소 → 자유 염소 증가 → 살균력 회복<br>
                                                                                        &nbsp;&nbsp;· 소독제의 효율 극대화.<br>
                                                                                    </span>
                                                                            </sup></li>   
                                                                        <li><span style="color: blue; font-weight: bold;">중화제(매직풀20)</span>
                                                                        <sup>
                                                                            <span class="tooltip" style="color: blue;">[1]
                                                                                <span class="tooltip-text">주로 수영장 물의 pH가 지나치게 높거나 낮을 때 이를 조절하는 데 사용되며, 알칼리성 중화제입니다. <br>
                                                                                    
                                                                                </span>
                                                                        </sup></li> 
                                                                             
                                                                    <li><span style="color: blue; font-weight: bold;">차아염소산나트륨(매직풀)</span>
                                                                        <sup>
                                                                            <span class="tooltip" style="color: blue;">[1]
                                                                                <span class="tooltip-text">차아염소산나트륨(NaOCl)은 염소 소독제의 주성분으로, 수영장 물을 소독하는 데 자주 사용됩니다. 주로 물속의 박테리아, 바이러스, 곰팡이, 조류 등을 살균하거나 소독하는 데 매우 효과적인 화학 물질입니다.<br>
                                                                                </span>
                                                                        </sup></li> 
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">사용방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">PH감소제</th>
                                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                            <li>설명</li>
                                                                        </ul>
                                                                    </td>
                                                                    
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>

                    <h3 id="section4-4" onclick="toggleSection('skill 4.4.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 4.4. 수영장 배수
                    </h3>

                        <div id="skill 4.4." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                <!-- 내용 -->
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>

                     <h3 id="section4-5" onclick="toggleSection('skill 4.5.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 4.5. 수영장 담수
                    </h3>

                        <div id="skill 4.5." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                <!-- 내용 -->
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>

                     <h3 id="section4-6" onclick="toggleSection('skill 4.6.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 4.6. 수영장 수온 관리
                    </h3>

                        <div id="skill 4.6." class="content hidden" style="margin-left: 20px;">
                            <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                <tr>
                                    
                                    <td>
                                        <div id="detailTable0" class="details">
                                            <table style="width: 100%; border-collapse: collapse; text-align: center;">

                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주요구성</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                <!-- 내용 -->
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                <tr>
                                                    <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">방법</th>
                                                    <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                        <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                            <table style="width: 100%; border-collapse: collapse;">
                                                                <tr>
                                                                    <li>수영장 열교환기의 환수온도를 설정한다.</li>
                                                                    <li>수영장 밸브를 조절하여 올라가는 속도를 조절한다.</li>
                                                                </tr>
                                                            </table>
                                                        </ul>
                                                    </td>
                                                </tr>
                                                
                                            </table>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>
                
                </li>
            </ul>

            <h2 id="section5" onclick="toggleSection('skill5')">5. 가스</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                
                </li>
            </ul>

            <h2 id="section6" onclick="toggleSection('skill6')">6. 건축</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                
                </li>
            </ul>

            <h2 id="section7" onclick="toggleSection('skill7')">7. 기타 주요업무</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                
                </li>
            </ul>

            <h2 id="section8" onclick="toggleSection('skill8')">8. 업체 연락처</h2>
            <ul style="list-style-type: none; padding-left: 0;">
                <li lass="underline" style="margin-left: 20px;">
                    <h3 id="section8-1" onclick="toggleSection('skill 8.1.')" style="cursor: pointer;">
                        <span class="arrow collapsed">></span> 8.1. 업체 연락처
                        </h3>
        
                        <!-- 펼치기/접기 내용 영역 -->
                            <div id="skill 8.1." class="content hidden" style="margin-left: 20px;">
                                <table style="width: 80%; margin: 0; border-collapse: collapse; text-align: center; font-size: 18px; white-space: nowrap;">
                                    <tr>
                                        
                                        <td>
                                            <div id="detailTable0" class="details">
                                                <table style="width: 100%; border-collapse: collapse; text-align: center;">
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">보일러</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                    010-3438-9524 이기쁨 기사(보일러 서비스)<br>
                                                                    010-3232-6954 박홍주 이사(보일러시운전)
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">건축 시공사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                    010-5504-6647 서원택 차장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">기계설비</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                    010-4067-8270 한상용 소장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">전기시공사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-7488-5822 이병철 부장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">에어컨 신규 설치 관련 전기공사 견적</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-4602-1839 맹주성 부장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">수질현황 전관판</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-4578-4638 유익현 사장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">에어컨 이전설치</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8005-0844 이성진 과장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">카드단말기</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8327-2805 금융결제원
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">주차관제</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        043-233-1583 현정보
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">소방시공사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5462-3220 지은성 소장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">외벽패널</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8705-5837 김인선 대표
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">에어커튼</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-4025-3718 김순화 대표
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">통신 선로 공사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-9229-1181 정주훈 이사
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">로지 시스템</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8983-8504 서용주 주임
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">차염발생기</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-9412-2091 정찬호 과장(퇴수구 막힘)<br>
                                                                        010-3208-9695 남진수 팀장(설치/관리)
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">역세 수처리설비 및 측정장비</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-7642-1018 이두성 차장
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">배구지주</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-6422-7367 안광욱대표
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">온수가열기</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8981-0322 박진수 팀장(영업)<br>
                                                                        010-3411-6615 황춘기 차장(납품 시공)
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">보일러 설치검사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-6894-6031 송진석 대리
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">방충망</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5615-2199 김현호 대리<br>
                                                                        010-5618-1341 이재빈 대리(A/S)
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">가스시공사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5218-0659 박정복 전무 <br>
                                                                        010-4592-3621 필터청소
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">수위조절판</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8075-1945
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">배구지주</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-6422-7367 안광욱대표
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">sk통신망 설치</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8567-0852
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">전화설치</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5466-8039 김천웅 이사
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">방송장비 납품 및 서비스</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-2661-3683 이도희 대표
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">공조기</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-8901-8078 백종호 이사
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">Kt 통신사</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-9331-4563 
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">외부간판전기업체</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5461-2364 광운전력
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">외부간판업체</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-5483-9499 비즈디자인
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                    <tr>
                                                        <th style="border: 1px solid #ccc; padding: 10px; white-space: nowrap;">수영장 청소기</th>
                                                        <td colspan="8" style="border: 1px solid #ccc; text-align: left;">
                                                            <ul style="list-style-type: disc; padding-left: 20px; margin: 0;">
                                                                <table style="width: 100%; border-collapse: collapse;">
                                                                    <tr>
                                                                        010-9231-4076 수영장 나라
                                                                    </tr>
                                                                </table>
                                                            </ul>
                                                        </td>
                                                        
                                                    </tr>
                                                </table>
                                            </div>
                                        </td>
                                    </tr>
                                </table>
                            </div>

                </li>
            </ul>
        
            <script>
                function toggleSection(sectionId) {
                    var section = document.getElementById(sectionId);
                    var arrow = section.previousElementSibling.querySelector('.arrow');
                    var isExpanded = section.style.display === "block";
    
                if (isExpanded) {
                section.style.display = "none";
                arrow.classList.remove('expanded');
                arrow.classList.add('collapsed');
                } else {
                section.style.display = "block";
                arrow.classList.remove('collapsed');
                arrow.classList.add('expanded');
                }
                }
            </script>
            <!-- 메인 콘텐츠 영역 -->
    
</div>
    <!-- JavaScript 코드 -->
    <script>
        function openPopup(src) {
            document.getElementById("popup-img").src = src;
            document.getElementById("popup").style.display = "flex";
        }
    
        function closePopup() {
            document.getElementById("popup").style.display = "none";
        }
    </script>
    
</body>
</html>
