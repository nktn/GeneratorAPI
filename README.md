
# yeoman-generator

## Link's

 + [yeoman-generator](https://github.com/yeoman/yeoman/wiki/Generators#wiki-frequently-asked-questions)

 + [GeneratorAPI](http://yeoman.github.io/generator/)

 + [Testing-generators](https://github.com/yeoman/generator/wiki/Testing-generators)

## Generator API's

### Module: [yeoman-generator](http://yeoman.github.io/generator/module-yeoman-generator.html)

| Member | infomation |
|:--|:--|
| assert      | テスト用のアサートヘルパ(Module: test/assert) |
| file        | グローバルファイルヘルパ(https://github.com/SBoudrias/file-utils) |
| generators | Yeoman generators 本体 (yeoman.Baseとyeoman.NamedBaseがデフォルト) |
| inquirer    | [非推奨]照会モジュールへの参照を得る |
| test        | テスト用のヘルパ( module:test/helpers) |


### Module: [test/assert](http://yeoman.github.io/generator/assert.html)

 + Node.jsのassertモジュールとMixes inする。

| Method | argment | infomation |
|:--|:--|:--|
| file | pairs(Array) | 配列の各ファイルが存在する事を確認する |
| file | file(String) | 指定されたファイルが存在する事を確認する |
| file | file(Sring), reg(Regex) | 指定された正規表現にマッチするファイルが存在する事を確認する |
| fileContent | file(String), reg(Regex) | ファイルの内容が正規表現にマッチすることを確認する。 |
| fileContent | pairs(Array) | fileContent(String, reg)のペア（配列渡し） |
| files | pairs(Array) | 配列で渡されたファイルが存在することを確認する、Arrayの中身がさらにArrayの場合に第2引数が正規表現の場合はファイルの中身を確認する |
| implement | subject(Object), methods(Object or Array) | オブジェクトに指定されたインタフェースが存在するかを確認する |
| noFile | file(String) | ファイルが存在しないことを確認する |
| noFile | pairs(Array) | 配列の各ファイルが存在しない事を確認する |
| noFileContent | file(String), reg(Regex) | ファイルの内容が正規表現にマッチしないことを確認する。 |
| noFileContent | pairs(Array) | noFileContent(String, reg)のペア（配列渡し） |
| textEqual | value(String), expected(String) | 2つの文字列が標準の改行コードも含めて同じことを確認する |


### Module: [test/helpers](http://yeoman.github.io/generator/helpers.html)

+ unit テストヘルパ コレクション(Mocha構文っぽい)

| Method | argment | infomation |
|:--|:--|:--|
| before | dir (String)| ``test``ディレクトリをクリーンアップし、ダミーGruntfile.jsを作成するMochaのBeforeへのコールバック関数を作成できます。 |
| createDummyGenerator | - | 簡単なダミージェネレータを作成します。 |
| createGenerator | name(String), dependencies(Array), args(Array or String), options(Object) | 依存関係、引数等を指定して柔軟にジェネレータを作成する |
| decorate | context(Object), method(String), replacement(function), options(Object) | カスタム機能を持つメソッドを挿入する |
| gruntfile | options, done | 
| mockPrompt | generator, answers | 
| restore |  | 
| run | Generator |  
| setUpTestDirectory | dir |  
| stub | context, method, replacement | 
| testDirectory | dir, cb | 
