# 今日やること

1. 環境構築

	ダメそうなので、私の環境を使います。 

	本来は、git for windowsもしくはgit (wsl,cygwin, minGW)を使います。
	
	* [git for windows](https://gitforwindows.org)
	* [https://www.cygwin.com/](https://www.cygwin.com/)

2. 概念説明
3. 実演

# gitとは

ファイルのバージョンを管理するツールである。
類似のものとして、次のものがある。

* sub version (svn)
* hg

といったものがあるが、それらは割愛する。

gitの特色として、分散型であることが挙げられる。cf. branch

# なんで必要になるのか
* 複数人で作業をするため。
  + ファイル共有の手段として
* コードの履歴を残したいから
  + バグが起きたときに、そのバグのコードだけを無効化することや巻き戻すことが
    容易にできる。 

# どうやって使うの?

* 空のリポジトリの作成: `git init`
   + `.git`というディレクトリが作られる。
   + vscodeでもコマンドパレットから生成可能。C-p,git initで検索
* 状況確認: `git status`
* ファイルの変更を登録する。: `git add <ファイル名>`
	+ まとめて登録する。:`git add -A`
* ファイルの変更を登録を解除する。: `git reset <ファイル名>`
* 変更を保存する: `git commit`
* 変更の履歴を確認する: `git log`
* ブランチを作成する: `git checkout -b <新しく作りたいブランチ>`
  + ブランチ名は`<ユーザー>/<機能>` 
* ブランチを移動する: `git checkout <ブランチ名>`
* ブランチを統合する: `git merge <ブランチ名>`
* GitHubにアップロードする
  + GitHubにリポジトリを作る。 
  + アップロード先を登録する:`git remote add origin <url>`
  + アップロードする:`git push origin <ブランチ名>` 
* GitHubからダウンロードする
  + 最初の一回目: `git clone <url>` 
  + 変更を確認する: `git fetch origin`
  + 変更を取り込む: `git pull origin <GitHubのブランチ名>`
* 重要なコミットにはタグを打つ。: `git tag <タグ名>`
  + タグはbranch同様にcheckoutで移動できる。
  + タグはpushして共有できる。 
* 実はエディタの機能を使うと楽ができる。

# 補講

## CLIとは

いつも使っているGUIの対義語。テキストでやり取りするもの。

## Linuxのコマンド

* `cd` ディレクトリの移動
* `mkdir` ディレクトリの作成
* `ls` ディレクトリの確認
* `pwd` 現在のディレクトリの確認
* `apt update` パッケージの情報を更新する
* `apt upgrade` パッケージを更新する
* `apt install <package>` パッケージをインストールする

## Markdownとはなにか

軽量マークアップ言語と呼ばれる。要は、HTMLを楽に書く方法の一つ。

* `#`をタイトルになる。`#`の数が多いほど、小さくなる(小見出しになる)
* `*`,`+`,`-`が箇条書きになる
* `1.`,`2.`のようにすると数字で箇条書される。
* `*`で囲むと強調される。(*b*,**b**)
* ```で囲むとコードブロックを意味する
```c
#include <stdio.h>

int main (int argc,char *argv){
	printf("hello world");
	return 0;
}

```

レスポンスすればいいですか
おｋです
もう一回言ってもらっていいですか

名前書いてってね
西永(なが)
小野(ゆーた)
辻岡（すず）
たいち（sabanekko
小林翼（赤）