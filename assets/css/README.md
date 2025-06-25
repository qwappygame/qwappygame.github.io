# CSS 폴더

이 폴더는 회사 홈페이지의 스타일시트 파일들을 관리합니다.

## 파일 구조 권장사항

### `main.css` 또는 `style.css`
- 메인 스타일시트 파일
- 전체 사이트의 기본 스타일 정의

### `components/`
- 컴포넌트별 CSS 파일들
- 예: `header.css`, `footer.css`, `hero.css`

### `pages/`
- 페이지별 특화 스타일
- 예: `home.css`, `about.css`, `contact.css`

### `utilities/`
- 유틸리티 클래스들
- 예: `spacing.css`, `typography.css`

## 사용 방법

Jekyll에서 CSS를 포함할 때는 다음과 같이 사용합니다:

```html
<!-- 기본 스타일시트 -->
<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">

<!-- 페이지별 스타일시트 -->
<link rel="stylesheet" href="{{ '/assets/css/pages/home.css' | relative_url }}">
```

## CSS 작성 가이드라인

1. **모듈화**: 기능별로 파일을 분리하여 관리
2. **네이밍**: BEM 방법론 등 일관된 네이밍 컨벤션 사용
3. **반응형**: 모바일 퍼스트 접근법 적용
4. **성능**: 불필요한 중복 제거 및 최적화 