# 바닐라 JS 프로젝트 성능 개선
- url: https://front-5th-chapter4-2-basic-alpha.vercel.app/

# 성능 개선 보고서

## 초기상태

### 🎯 Lighthouse 점수
| 카테고리 | 점수 | 상태 |
|----------|------|------|
| Performance | 72% | 🟠 |
| Accessibility | 82% | 🟠 |
| Best Practices | 75% | 🟠 |
| SEO | 82% | 🟠 |
| PWA | 0% | 🔴 |

### 📊 Core Web Vitals (2024)
| 메트릭 | 설명 | 측정값 | 상태 |
|--------|------|--------|------|
| LCP | Largest Contentful Paint | 14.71s | 🔴 |
| INP | Interaction to Next Paint | N/A | 🟢 |
| CLS | Cumulative Layout Shift | 0.011 | 🟢 |

### PageSpeed Insights 측정 결과
![Image](https://github.com/user-attachments/assets/f0fbcee6-7d6f-4035-8122-e6672d0c6c86)


## 개선 사항
1. 이미지 최적화
   - 이미지 jpg,png -> webp 변경 및 사이즈 축소
   - aspect-ratio와 object-fit 속성 추가로 이미지 왜곡 방지
2. 쿠키 동의 스크립트 개선:
   - 중복 로드 제거    
   - 버전 업그레이드 (4.1.0 → 4.2.0)
   - 동적 로딩 방식 유지
3. 보안 정책 개선:
   - Content Security Policy(CSP) 수정  
   - 'unsafe-inline' 제거로 보안 강화
   - 허용된 도메인만 명시적으로 지정

## 개선 후 상태

### 🎯 Lighthouse 점수
| 카테고리 | 점수 | 상태 |
|----------|------|------|
| Performance | 100% | 🟢 |
| Accessibility | 95% | 🟢 |
| Best Practices | 68% | 🟠 |
| SEO | 100% | 🟢 |
| PWA | 0% | 🔴 |

### 📊 Core Web Vitals (2024)
| 메트릭 | 설명 | 측정값 | 상태 |
|--------|------|--------|------|
| LCP | Largest Contentful Paint | 1.53s | 🟢 |
| INP | Interaction to Next Paint | N/A | 🟢 |
| CLS | Cumulative Layout Shift | N/A | 🟢 |

### PageSpeed Insights 측정 결과
![Image](https://github.com/user-attachments/assets/041317c3-b7c3-4ed3-bd21-9fb332893a3e)