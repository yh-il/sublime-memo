# sublime-memo
SublimeText3の初期設定のmemoです。

###公式サイト
[http://www.sublimetext.com/3](http://www.sublimetext.com/3)

※たぶんWindows64bit版落としてきてインストールすれば大丈夫

###Package Controlのインストール

View -> Show Consoleでコンソールを開いて以下のコードをコピペ→Enter

```
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

###いつも入れるパッケージ
* IMESupport
* ConvertToUTF8
* Goto css Declaration
* Bracket Highlighter
* AutoFileName
* Emmet
* Hayaku
* SideBarEnhancements
* All Autocomplete
* jQuery
* HTML5
* Better JavaScript
* DocBlocker
* LiveStyle(Chrome拡張機能もインストールする必要あり)
* View in Brouser
* HTML CSS JS Prettify
* InputSequence(連番入力のやつ)→https://github.com/kazu1107/InputSequence
* GitGutter(Gitを参照して変更箇所を表示してくれるやつ)
* SyncedSideBar(現在開いているファイルとサイドバーのファイルを一致させて表示してくれるやつ)
* YUI Compressor(CSS,JSのMinify化するやつ（ctrl + Bでコンパイル）※JAVAが必要)
* Color Highlighter(#ff00aaとかを実際の色で表示してくれる、カラーピッカー機能もついてる)
* SublimeLinter
* SublimeLinter-jshint(SublimeLinterとセットで入れて、npm install -g jshintも実行する)
* Sass
* Sass Build
* Bootstrap 3 Snipets
* eCSStractor(クラスをまとめて書き出してくれるやつ)

###キー設定

```
//Goto CSS Declarationの設定
 {
    "keys": ["ctrl+alt+."], "command": "goto_css_declaration",
    "args": {"goto": "next"}
 },
 {
    "keys": ["ctrl+alt+,"],  "command": "goto_css_declaration",
    "args": {"goto": "prev"}
 },

 // 上の行と入れ替える
{ "keys": ["alt+up"], "command": "swap_line_up" },
// 下の行と入れ替える
{ "keys": ["alt+down"], "command": "swap_line_down" },

// F3で関数の宣言元にジャンプ
{ "keys": ["f3"], "command": "goto_definition" },
// alt+左で戻る
{ "keys": ["alt+left"], "command": "jump_back" },
// alt+右で戻ったのをまた進める
{ "keys": ["alt+right"], "command": "jump_forward" },
```

###関数ジャンプをalt+Clickで行う

Preferences > Browse Packagesで設定ファイルが入っているディレクトリを開いて
更にUserディレクトリの中にDefault (Windows).sublime-mousemapというファイルを作成し、
中に以下の設定を書くと反映されました。

```
[
    {
        "button": "button1", 
        "count": 1, 
        "modifiers": ["alt"],
        "press_command": "drag_select",
        "command": "goto_definition"
    },
]
```

###ユーザ設定

Preference > Setting User (ユーザー設定)

```
{
	"afn_insert_width_first": true,
	"auto_complete": true,
	"auto_complete_commit_on_tab": true,
	"color_scheme": "Packages/Theme - Flatland/Flatland Monokai.tmTheme",
	"default_encoding": "UTF-8",
	"default_line_ending": "system",
	"font_face": "MigMix 1M",
	"font_size": 11,
	"highlight_modified_tabs": true,
	"ignored_packages":
	[
		"Vintage",
		"JavaScript"
	],
	"scroll_past_end": true,
	"show_encoding": true,
	"show_line_endings": true,
	"theme": "Flatland Dark.sublime-theme"
}
```

###BracketHighlighterの設定
```
{
  "ignore_threshold": true // サーチ範囲を限定しない
}
```


##Color Scheme
```
One Dark(Atomのやつ)
```

