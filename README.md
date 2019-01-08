フォント作成関連の情報をまとめます。  
Glyphs/FontForge/AFDKOを使う予定でしたが、  
Glyphsで事足りるかもしれないのでグリフスの情報まとめになるかも？  


フォント作成の手引き。  
目標は源ノ明朝をベースフォントとして空のフォントを作成し、  
GlyphsあるいはFontForgeでコンパイルしてOTFフォントを作ることを目標とします。  
①．グリフスで源ノ明朝を開く  
　　これはそのままできるはず  

②．0000/0001のみを活かして他を削除する  
　　グリフが空のフォントを作成するため  
　　0000/0001のフォントは無いとエラーになるようなので設定したままとします。  

③．この段階でグリフスファイルとして保存する。  
　　SourceHanSerif-Regular-c.glyphs  

④．まずそのままフォントの書き出し出力をしようとしてみる。→コンパイルエラーになるはず  
　　line too long エラーが現れる。  
　　Glyph名に128字以上の名前がついているときこのエラーになるようなので  
　　128字以上の名前がついているグリフの名前を変更する。  
　　登録情報は変えず名前だけ変えたい  
　　グリフ検索では正規表現が使用できるので .{128,} とするとグリフ検索をすることができる。  
　　フォント出力に含めないオプションを有効にしてみて、  
　　名前を変更しないでみる。  

⑤．この状態でフォント出力してみると？？？  
　　→  
　　makeotfGlyphs [FATAL] line too long [GlyphOrderAndAliasDB 60692]  
　　やはりエラー  
　　フォント名を改名するとその他という分類になってしまうのだけど、改名してみる  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han  
を128字以下の名前に変更する。  
AboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han  
を128字以下の名前に変更する。  
AboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han  

　　それでもエラーになったので以下を操作。  
　　iボタンから開けるフォント情報内のフューチャーのタブを開く、  
　　まずccmp(合字)フューチャー内のフォント名も、改める。  
descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED3_descriptionAboveToBelow_uni2F94_uni2EE2_descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  
を128字以下の名前に変更する。  
descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

　　ccmpフューチャーを全部更新してフォント出力してみると？？？  

⑥．token to too long エラーになる。  
　　ccmpフューチャーのトークンはmax length 63 らしいので 63 以下に削る。  
　　A-59-L  
　　descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  
　　B-59-L  
　　descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  
　　に更新する。  

　　グリフ名を 59 に、token length を 59 に改めてフォント出力してみると？？？  
　　not in font エラーとなるので出力対象に含めてやってみると？？？  
　　cid65533" (alias "descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han") not in font  
　　というエラーがでる。これの対処法を調べないとならない。  
　　直し方が不明であるので ccmp フューチャーから該当マッピングを消してみると。  

　　ccmp フィーチャー 5 行目の“Glyph "cid65533" (alias "descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han") not in font”  

　　L5を消す  
sub descriptionSurroundFromLowerLeft-han uni2ECD descriptionAboveToMiddleAndBelow-han uni2F73 descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93 uni2ED1 descriptionAboveToBelow-han uni2F94 uni2FBA descriptionAboveToBelow-han uni2E93 uni2ED1 uni2E89 uni2F3C by descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  

　　エラー：ccmp フィーチャー 5 行目の“Glyph "cid65534" (alias "descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han") not in font”  
　　sub descriptionSurroundFromLowerLeft-han uni2ECD descriptionAboveToMiddleAndBelow-han uni2F73 descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93 uni2ED3 descriptionAboveToBelow-han uni2F94 uni2EE2 descriptionAboveToBelow-han uni2E93 uni2ED3 uni2E89 uni2F3C by descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

　　エラー：ccmp フィーチャー 5 行目の“Glyph "cid65533" (alias "descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han") not in font”  
　　sub descriptionSurroundFromLowerLeft-han uni2ECD descriptionAboveToMiddleAndBelow-han uni2F73.jp78 descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93 uni2ED1 descriptionAboveToBelow-han uni2F94 uni2FBA descriptionAboveToBelow-han uni2E93 uni2ED1 uni2E89 uni2F3C by descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han;  

　　エラー：ccmp フィーチャー 5 行目の“Glyph "cid65534" (alias "descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han") not in font”  
　　sub descriptionSurroundFromLowerLeft-han uni2ECD descriptionAboveToMiddleAndBelow-han uni2F73.jp78 descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93 uni2ED3 descriptionAboveToBelow-han uni2F94 uni2EE2 descriptionAboveToBelow-han uni2E93 uni2ED3 uni2E89 uni2F3C by descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

　　エラー：ccmp フィーチャー 6 行目の“Glyph "cid65534" (alias "descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han") not in font”  
　　sub descriptionSurroundFromLowerLeft-han uni2ECD.locl descriptionAboveToMiddleAndBelow-han uni2F73.locl descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93.locl uni2ED3 descriptionAboveToBelow-han uni2F94.locl uni2EE2 descriptionAboveToBelow-han uni2E93.locl uni2ED3 uni2E89 uni2F3C.locl by descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

　　エラー：ccmp フィーチャー 7 行目の“Glyph "cid65534" (alias "descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han") not in font”  
　　sub descriptionSurroundFromLowerLeft-han uni2ECE descriptionAboveToMiddleAndBelow-han uni2F73.locl descriptionLeftToRight-han uni2F49 descriptionLeftToRight-han descriptionLeftToMiddleAndRight-han descriptionAboveToBelow-han uni2E93.locl uni2ED3 descriptionAboveToBelow-han uni2F94.locl uni2EE2 descriptionAboveToBelow-han uni2E93.locl uni2ED3 uni2E89 uni2F3C.locl by descriptionAboveToBelow_uni2E93_uni2ED3_uni2E89_uni2F3C-han;  

　　エラー：hist フィーチャー 1 行目の“Glyph "glyph67219" not in font (featMapGName2GID)”  
　　sub i-bopomofo by ih-bopomofo;  

　　エラー：locl フィーチャー 13079 行目の“token too long; max length is 63 (text was "descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han")”  
　　sub descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61037;  
　　→  
　　descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61037;  

　　エラー：locl フィーチャー 13079 行目の“Glyph "cid65533" (alias "descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han") not in font”  
　　デリート  
　　sub descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61037;  

　　エラー：locl フィーチャー 26570 行目の“token too long; max length is 63 (text was "descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han")”  
　　→  
　　sub descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61038;  
　　→  
　　デリート  
　　sub descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61038;  

　　このエラーに変わってしまう。  
　　GSUB feature 'locl' causes overflow of offset to a subtable (0x11ab4)  

　　L26570を戻してコンパイル  
　　エラー：locl フィーチャー 26570 行目の“Glyph "cid65533" (alias "descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han") not in font”  
エラー：locl フィーチャー 39672 行目の“token too long; max length is 63 (text was "descriptionSurroundFromLowerLeft_uni2ECD_descriptionAboveToMiddleAndBelow_uni2F73_descriptionLeftToRight_uni2F49_descriptionLeftToRight_descriptionLeftToMiddleAndRight_descriptionAboveToBelow_uni2E93_uni2ED1_descriptionAboveToBelow_uni2F94_uni2FBA_descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han")”  

　　こうなるので、オーバーフローエラーを抑制するため 26570 行目を書き換える  
26570 sub descriptionAboveToBelow_uni2E93_uni2ED1_uni2E89_uni2F3C-han by cid61038;  
26570   

　　これでもエラーになる  

　　今度は 26570 行目の含まれるロケーションごと消してみる  
　　
　　locl のテーブルごと削除したらコンパイルは通る。  
　　
　　locl テーブルを極限まで最小化してみてもコンパイルが通るようになった。  
　　これで問題ないかもしれない。  

⑦．完成済みフォントから1字形のグリフだけコピーしてくる。  
　　その状態でフォントの書き出しを行って成功したので、  
　　源ノ明朝のCIDmapingに由来する空のフォントの作成に成功したということになる。  
　　このフォントは日本語・韓国語・中国語の字形を含め65535グリフの枠を保有するフォントである。  

　　2019/01/08現在、仮に、uni67B4 おうこ の字だけマッピング内に使える字形を入れてみてあります。

