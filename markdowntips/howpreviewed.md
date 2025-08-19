# MarkdownファイルがGitHubでプレビューされるまでの仕組み

## MarkdownはまずGitHubのサーバーでHTMLに変換され、そしてからナニやらカニやらされる

Markdown記法を開発したJohn Gruber氏は、自身のブログで下記のように紹介しています。

> Markdown is a text-to-HTML conversion tool for web writers.
> Markdown allows you to write using an easy-to-read, easy-to-write plain text format,  
> then convert it to structurally valid HTML.

    （日本語訳）Markdownは、ウェブライター向けのテキストからHTMLへの変換ツールです。  
    Markdownを使用すると、読みやすく書きやすいプレーンテキスト形式で文章を作成し、  
    その後構造的に正しいHTMLに変換することができます。

Markdownは実際、GitHubでプレビューされる際には、まずHTMLに変換されます。

私がChatGPTに聞いたところによると、プレビューされるまでの仕組みはこうです。

1. **MarkdownをGitHubリポジトリにpush**　→この時点ではMarkdownもただのテキスト
2. **GitHubのサーバーがMarkdownをHTMLに変換**
3. **そのHTMLに、GitHub内蔵のCSSが適用される**　→見出しが大きな文字になり、表は表のような見た目となり、文字間行間もGitHub風に整えられる
4. **GitHubに組み込まれたJavaScriptで動きを追加**　→外部リンクの挙動制御とかされる
5. **ブラウザでプレビューされる**　→私達がブラウザでプレビューページを開くと、#や-などはそれぞれ整えられて見えず、通常のウェブページのような見た目の画面が見える

## MarkdownはHTMLを簡単に書くための記法

Markdownはあくまでも**HTMLファイルを簡単に作成するためのもの**だったのですね。


やはりAIフレンドリーな情報管理やデザイン設計の方法を編み出すには、HTMLの学習が必要だと私は認識しました。

