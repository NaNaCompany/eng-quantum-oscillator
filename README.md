# 양자 조화진동자 에너지 계산기

영점에너지를 포함하는 1차원 양자 조화진동자의 에너지 준위를 계산한다.

- ID: E114
- App: https://nanalab.kr/eng-quantum-oscillator/
- Repository: https://github.com/NaNaCompany/eng-quantum-oscillator
- Formula: Eₙ = ℏω(n+1/2)

## Model and data

ω>0이며 n은 0 이상의 정수다. 평형점의 위치에너지를 0으로 정한 이상적인 포물선 퍼텐셜을 사용한다. 비조화성·감쇠·상호작용·상대론 보정은 제외한다. 입력은 Hz 주파수 f가 아니라 각진동수 ω이며 ω=2πf이다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
