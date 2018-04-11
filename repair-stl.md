## 3d プリントに向けての STL ファイルの修復  


#### netfabb  
同名の Autodesk の有料サービスがあるが、こっちは無料。  
google login で使える。  

[https://service.netfabb.com/login.php](https://service.netfabb.com/login.php)  

データによって、アップロードエラーが出る。  
（アップロードエラーがでたものを、DMM.Make などに投げると、造形可能と帰ってくるので、破損しているとかとは違うっぽい）  

手元に破損した都合の良い STL がなかったので、検証してません。。。  



---  

あとは、Rhino でのこと。  

Rhino で、Open Mesh をどう処理するか結構よくわからない。  
Rhino で出てくるのはこの辺。  

Open Brep, Open Mesh  
Invalid Brep, Invalid Mesh(見たことないかな？)  
Closed Brep, Closed Mesh  

---  

3D プリントするなら、Closed Mesh でなければいけない。  

Open Mesh は、fillHole 系の コマンドか、Brep の段階で、cap/capEx で閉じたい。  

これが、できないことがあるので、ほんとは grasshopper でエッジを探して中点とって、メッシュを構築して、みたいのがあったら良さそう。  

Invalid のほうは、正直よくわからないが、  
Brep の時は、 Explode して、 Invalid な Surface を特定してそれだけ作り直す、くらいしかわからない。
