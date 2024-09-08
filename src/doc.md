# Rsbuild: 次世代の高速ビルドツールを探る

## Rsbuild とは

- RsbuildはRspackを利用した高性能なビルドツール
- ByteDance社のWeb Infra team（web-infra-dev）が開発している
  - RspackやRsbuild・Rspressなど多くのツールが存在
  - メンバーにはOXCの作者やWebpackのコアメンバーが在籍

### Rspackとは

- Webpackと相互運用を提供するRust製の高速バンドラー
- Webpackとの完全な互換性を目指すものではなく、一定成熟した段階でWebpackとRspackを統合することを目指している
  - そのために、webpackチームとのパートナーシップが確立されている
https://rspack.dev/misc/faq

## Vite・Vue CLI・CRAとの比較

- Rsbuild は Vite と Vue CLI と同等のビルドツールを提供している
- Vue CLI・CRAとの比較
  - 基盤がWebpackからRspackに切り替えられ、ビルドパフォーマンスが5〜10倍向上
  - React・Vueなどのフレームワークからは分離されているため、それぞれのプラグイン経由でSvelteなどでも利用ができる
  - 豊富な拡張機能を提供している
    - https://rsbuild.dev/config/
- Viteとの比較
  - RsbuildはViteと多くの類似点を持っている
  - Webpackプラグインのほとんどとの互換性やRspackプラグイン全てとの互換性を持っている
    - ViteはRollup.jsプラグインとの互換性を持つ
  - 現在のプロダクトがWebpackとの互換性を多く持っている場合、Rsbuildへの移行は比較的容易


## ビルドパフォーマンス

https://github.com/web-infra-dev/rsbuild?tab=readme-ov-file

## サポートされているフレームワーク

- TypeScript
- CSS
- HTML
- React・Preact
- Vue
- Svelte
- NestJS

## サポート予定

- Nuxt.js
  - 開発ビルドに導入予定のPRが進行中
  - https://github.com/nuxt/nuxt/pull/20067
- Next.js
  - 最新を常に追ってないのでこっちは分からん
  - 社内のReact・Next使っている人は最新追ってるはずなんで聞いてみて
