# 이미지 폴더 구조

이 폴더는 회사 홈페이지에서 사용되는 모든 이미지 파일들을 체계적으로 관리하기 위한 구조입니다.

## 폴더 구조

### `/logo`
- 회사 로고 이미지들
- 다양한 크기와 형식의 로고 파일
- 예: `company-logo.png`, `company-logo-white.svg`, `favicon.ico`

### `/hero`
- 메인 페이지 히어로 섹션 이미지들
- 배너, 슬라이더에 사용되는 대형 이미지
- 예: `hero-banner.jpg`, `main-slider-1.jpg`

### `/team`
- 팀원 프로필 사진들
- 회사 소개 페이지에 사용
- 예: `ceo-profile.jpg`, `team-member-1.jpg`

### `/products`
- 제품/서비스 관련 이미지들
- 제품 카탈로그, 포트폴리오에 사용
- 예: `product-1.jpg`, `service-icon.png`

### `/blog`
- 블로그 포스트에 첨부되는 이미지들
- 각 포스트별로 하위 폴더 생성 권장
- 예: `2024-01-15-post-image.jpg`

### `/icons`
- 아이콘 이미지들
- UI 요소, 소셜 미디어 아이콘 등
- 예: `facebook-icon.svg`, `arrow-right.png`

### `/backgrounds`
- 배경 이미지들
- 섹션 배경, 패턴 등에 사용
- 예: `section-bg.jpg`, `pattern.png`

## 사용 방법

Jekyll에서 이미지를 사용할 때는 다음과 같이 경로를 지정합니다:

```html
<!-- 로고 이미지 -->
<img src="{{ '/assets/images/logo/company-logo.png' | relative_url }}" alt="회사 로고">

<!-- 히어로 이미지 -->
<img src="{{ '/assets/images/hero/hero-banner.jpg' | relative_url }}" alt="메인 배너">

<!-- CSS에서 배경 이미지 -->
<style>
.hero-section {
    background-image: url('{{ "/assets/images/hero/hero-bg.jpg" | relative_url }}');
}
</style>
```

## 이미지 최적화 권장사항

1. **파일 크기**: 웹 최적화를 위해 적절한 압축 사용
2. **형식**: 
   - 사진: JPG (고품질), WebP (최신 브라우저)
   - 아이콘/로고: SVG, PNG
3. **반응형**: 다양한 화면 크기에 대응하는 이미지 준비
4. **alt 텍스트**: 접근성을 위한 대체 텍스트 필수 