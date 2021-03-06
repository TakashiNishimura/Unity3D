# Unity 入門

* 実行環境：Unity 2017.2 Personal 以降 / Ubuntu 16.04.4 LTS 以降

### <b>INDEX</b>

|No.|タイトル|内容|WebGL|.apk|project|参考資料|
|:--:|:--|:--|:--:|:--:|:--:|:--:|
|000|[インストール](https://github.com/mubirou/HelloWorld/blob/master/languages/C%23Unity/C%23Unity_linux.md)|開発環境（Linux版）の構築|－|－|－|－|
|001|[プリミティブ･オブジェクト](#プリミティブ･オブジェクト)|立方体･球･カプセル･円柱･平面の利用|－|－|－|－|
|002|[Blenderからの読み込み](#002)|Blenderで加工したモデルをインポート|－|－|－|－|
|003|[入門動画](#入門動画)|入門者向けの解説動画|－|－|－|－|
|004|[『Unityで神になる本。』](#004)|参考書の勉強|[●](#Unityで神になる本)|－|－|[●](https://amzn.to/2s85DAv)|
|005|[ユーザー設定](#ユーザー設定)|初期設定では使いにくい設定を変更|－|－|－|－|
|006|[マウス操作](#マウス操作)|個人的に必須のマウス操作|－|－|－|－|
|007|[出力](#出力)|Unityで作成したプロジェクトを出力する方法|－|－|－|[●](https://amzn.to/2s85DAv)|
|008|[VideoPlayerコンポーネント](#008)|VideoPlayerコンポーネントによる動画ファイル再生|－|－|－|－|
|009|[『Unity 2018 逆引き大全 300の極意』](#逆引き大全)|参考書の勉強|－|[●](#逆引き大全)|－|[●](https://amzn.to/2KuNW69)|
|010|[Analog Watch](#010)|「Hello world!」的コンテンツ|－|－|[●](#010)|－|
|011|[Drop Hole](#011)|「物理エンジン」を使ったゲーム|－|－|[●](#011)|－|
|012|[Stop Watch](#012)|uGUI（Text･Button）と外部フォントを使用|－|－|[●](#012)|－|
|013|[Mouse Stalker](#013)|（マウスに）追従|－|－|[●](#013)|－|
|014|[UFO Shooting](#014)|衝突判定･パーティクルを使用|－|[●](#014)|[●](#014)|－|
|015|[Timeline Anime](#015)|Animation･Timelineを使ったアニメーション|－|－|[●](#015)|－|
|016|[Puppet Control](#016)|アクション付の3Dモデルのコントロール|－|[●](#016)|[●](#016)|－|
|017|[Humanoid](#017)|Blenderからの連携の基本（人間型）|－|－|[●](#017)|－|
|018|[AR入門](#018)|HelloAR|－|－|－|[●](https://amzn.to/2VY0ZSr)|
|019|[SQLite操作](#019)|Unity C#からSQLiteを操作|－|－|－|－|
***

<a name="プリミティブ･オブジェクト"></a>
# <b>001 プリミティブ･オブジェクト</b>

### 概要
* Unity内で作成できる基本的な形状。
* モデリング（変更）は不可。
* X･Y･Z方向への拡大･縮小は可能。
* 通常はテスト目的でプレースホルダーとして利用。
* [Inspector]-[Mesh Renderer] の ✔ を外して「当たり判定」の領域として使うことも可能。

### 作成方法
1. [GameObject]-[3D Object] を選択。
1. ①Cube ②Sphere ③Capsole ④Cylinder ⑤Plane ⑥Quad の中から選択。

### プリミティブの種類
1. Cube（キューブ）
    * 1x1x1の立方体。
    * 壁、柱、箱、階段などに利用。
1. Sphere（スフィア／球）
    * 直径1（半径0.5）の球。
    * 星・弾丸などに利用。
1. Capsole（カプセル）
    * 円柱（高さ1、直径1）の上下に半球（直径1）を加えたもの。
    * 物理挙動をテストするプロトタイプなどに利用。
1. Cylinder（シリンダー／円柱）
    * 高さ2、直径1の円柱。
    * 柱、棒、タイヤなどに利用。
1. Plane（プレーン／平面）
    * 10x10の平面（200個の三角形で構成）。
    * 床、壁などに利用。
1. Quad（クワッド）
    * 1x1の平面（2個の三角形で構成）。
    * 画像や動画の再生などに利用。  

![001](https://mubirou.github.io/Unity3D/introduction/jpg/001.jpg)

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年04月17日


<a name="002"></a>
# <b>002 Blenderからの読み込み</b>

### 3Dモデル無料素材の用意
* [Free3D](https://free3d.com/)にアクセス。
* 任意のモデル（.obj形式）を選択し [Download]。

### Blenderでインポート〜エクスポート
1. Blenderを起動（立方体は削除）。
1. [ファイル]-[インポート]-[wavefront(.obj)] で上記の "xxx.obj" ファイルをインポート。
1. 任意で修正。
1. [ファイル]-[エクスポート]-[FBX(.fbx)] からエクスポート。

### Unityにインポート
1. Unityを起動。
1. [Project]-[Create]-[Folder] を選び "Model001" フォルダを作成。
1. デスクトップ等にある "xxx.fbx" ファイルを、上記のフォルダにドラッグ＆ドロップ。
    * (Project name)/Assets/ フォルダ内に "xxx.fbx" ファイル等がコピーされます。
1. [Project]-[Model001] 内のモデルを [Hierarchy] にドラッグ＆ドロップ。
1. 必要に応じて色を変更するなど行います。

![002](https://mubirou.github.io/Unity3D/introduction/jpg/002.jpg)

実行環境：Unity 2017.2 Personal、Blender 2.79、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年04月18日


<a name="入門動画"></a>
# <b>003 入門動画</b>

|No.|内容|WebGL|視聴日|
|:--|:--|:--:|:--:|
|001|[板とボール+物理エンジン①](https://www.youtube.com/watch?v=ruAN7e4wRwg)|－|2018-04-20|
|002|[板とボール+物理エンジン②（反射係数）](https://www.youtube.com/watch?v=Km8TpJ850Yo)|－|2018-04-20|
|XXX|[XXX](#XXX)|－|－|

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年04月20日  
更新日：2018年0X月XX日


<a name="004"></a>
# <b>004 『Unityで神になる本。』</b>

頁数は [『Unityで神になる本。／廣鉄夫著』](https://amzn.to/2s85DAv) のページです。

|No.|内容|頁数|WebGL|.apk|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|:--:|
|01|天地創造。（プログラムレス）|33〜76|[●](https://mubirou.github.io/Unity3D/introduction/html/004_01/index.html)|－|[●](https://assetstore.unity.com/packages/essentials/asset-packs/standard-assets-32351)|2018-05-23|
|02|[考え方と構造。](#考え方と構造。)|77〜112|－|－|－|2018-07-08|
|03|[世界を構成するもの。](#世界を構成するもの。)|113〜164|－|－|－|2018-07-10|
|04|[スクリプト基礎知識。](#スクリプト基礎知識。)|165〜258|－|－|－|2018-07-17|
|05|[アニメーションとキャラクタ。](#アニメーションとキャラクタ。)|259〜290|－|－|－|2018-07-18|
|06|[GUIとAudio。](#GUIとAudio。)|291〜330|－|－|－|2018-07-18|
|07|[出力。](https://github.com/mubirou/Unity/tree/master/introduction#%E5%87%BA%E5%8A%9B)|331〜360|－|－|－|－|

<a name="考え方と構造。"></a>
### 02 考え方と構造。</b>

* [シーン](https://docs.unity3d.com/ja/current/Manual/CreatingScenes.html) : 1つのプロジェクトに作った複数のシーン間をスクリプトで移動可能（シーンは[ビルド](https://docs.unity3d.com/jp/current/Manual/PublishingBuilds.html)に含まなくても良い）
* [GameObject](https://docs.unity3d.com/ja/current/Manual/GameObjects.html) : 世界に配置されているモノの基本単位（[コンポーネント](https://docs.unity3d.com/ja/current/Manual/UsingComponents.html)の入れ物）･[Transform](https://docs.unity3d.com/ja/current/ScriptReference/Transform.html)コンポーネントがミニマム
* [Collider（コライダー）](https://docs.unity3d.com/ja/current/Manual/CollidersOverview.html) : 衝突判定の領域（①Box ②Sphere ③Capsuleの3つあり）
* [Rigidbody](https://docs.unity3d.com/ja/current/Manual/class-Rigidbody.html) : 物体としての属性を持たせる（[Add Component]-[Physics]-[Rigidbody]）
* [跳ね返り効果](https://docs.unity3d.com/ja/current/Manual/class-PhysicMaterial.html)（摩擦係数と反発係数）: [Project]-[Create]-[Physics Material]-[Inspector]-[Bounciness] の値を上げる → オブジェクト（Rigidbody済）の [Inspector]-[XXX Colider] の [Material] にドラッグ
* [Prefab（プレハブ）](https://docs.unity3d.com/jp/current/Manual/Prefabs.html) ≒ Flash MovieClip  
    * [Select] : 親を開く
    * [Revert] : 元のPrefab状態に戻す
    * [Apply] : 元のPrefabを自分と同じ状態に変更
* [スクリプト](https://docs.unity3d.com/ja/current/Manual/CreatingAndUsingScripts.html)とは?（Prefabを100個登場させる例文）
    ```
    //DropBox.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class DropBox : MonoBehaviour {
        public GameObject MyCube;
        private int _count = 0;

        void Start () {
            InvokeRepeating("HogeMethod", 0.0f, 0.1f); //0秒後から0.1秒毎に呼出す
        }

        void HogeMethod() {
            _count ++;
            Instantiate(
                MyCube,
                new Vector3(Random.Range(-2.0f, 2.0f), 10.0f, Random.Range(-2.0f, 2.0f)), 
                Quaternion.identity
                );
            if (_count == 100) {
                CancelInvoke();
            }
        }
    }
    ```
* [タブのロック](https://docs.unity3d.com/ja/current/Manual/InspectorOptions.html) : [Add Tab] で複数のGameObjectの情報を同時表示可能
* [属性のコピー](https://docs.unity3d.com/ja/current/Manual/UsingComponents.html) : [Inspector] 内の任意のComponentの ⚙ から [Copy Component] → [Past ...] でコピー

<a name="世界を構成するもの。"></a>
### 03 世界を構成するもの。</b>

* 音を作成する？（ありものを使う）  
    [freesound.org](https://freesound.org/) : 無料でダウンロード可能  
    [Asset Store](https://assetstore.unity.com/categories/audio) : Unityアセットストア  
* 2次元画像製作。  
    Unityでは実行時に再圧縮をかけるため予め[ダウンサイジングしておく必要はない](https://docs.unity3d.com/jp/current/Manual/class-TextureImporter.html)  
    Unity 2018.1 以降であれば [SVG](https://ja.wikipedia.org/wiki/Scalable_Vector_Graphics) ファイルを[読み込む方法](http://tsubakit1.hateblo.jp/entry/2018/05/22/233000)もあるとのこと  
* 3Dモデリングデータの読み込み方法  
    ①汎用モデルデータ（[.fbx](https://ja.wikipedia.org/wiki/FBX)）  
    ②ネイティブデータ（Unity環境に該当3Dツールがインストールされている必要がある）  
* おすすめ3Dツール  
    ①[Blender](https://blender.jp/) : 無料（Linux/macOS/Win）  
    ②[SketchUp Make](https://www.sketchup.com/ja) : 非商用は無料（macOS/Win）  
    ③[Shade 3D for Unity](https://shade3d.jp/product/shade-3d-for-unity/index.html) : 無料（macOS/Win）  
    ④[Cheetah3D](https://www.cheetah3d.com/) : $99（macOS専用)  
    ⑤[Metasequoia](http://www.metaseq.net/jp/) : 5400円〜（アニメーションには非対応/Win専用）  
    その他、[ZBrush](https://oakcorp.net/pixologic/)、[Maya LT](https://www.autodesk.co.jp/products/maya-lt/overview)、[CINEMA 4D Prime](https://oakcorp.net/maxon/)、[LightWave](http://www.dstorm.co.jp/lw2018/)、[MODO](http://modogroup.jp/modo) 等の高額なツールもある  
    ※Unityで使うのはモデリング等の一部の機能です
* Unity用モデリングの注意  
    * 有効なのは「マテリアル名」と「色情報」のみ（細かな質感とは無視される）  
    * [UVマップ](http://www.blender3d.biz/texturing_uvunwrapmappingtypes.html)は有効  
    * [サブディビジョンサーフェス](http://www.blender3d.biz/simple3dcg_modeling_smoothing.html)は有効
    * リギング（IK）やアニメーションデータは「.fbx」や「.blend」の利用で有効  
    ※[Adobe mixamo](https://www.mixamo.com/#/) : 自動リギング＆アニメーションサービスあり（有料）

<a name="スクリプト基礎知識。"></a>
### 04 スクリプト基礎知識。</b>

* スクリプトはシーン内のGameObjectのコンポーネントとして動作する  
    （どのGameObjectに追加しても良いが、通常わかりやすいところに記述する）
* デフォルトのコード（C#）
    ```
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class HelloWorld : MonoBehaviour {

        // Use this for initialization
        void Start () {
            
        }
        
        // Update is called once per frame
        void Update () {
            
        }
    }
    ```
* 主なイベント  

|イベント名|内容|
|:--|:--|
|[Awake](https://docs.unity3d.com/jp/current/ScriptReference/MonoBehaviour.Awake.html)|最初に実行される|
|[Start](https://docs.unity3d.com/jp/current/ScriptReference/MonoBehaviour.Start.html)|シーンのスタート時に一度だけ実行|
|[Update](https://docs.unity3d.com/ja/current/ScriptReference/MonoBehaviour.Update.html)|再生中画面がアップデートされる度に実行|
|[LastUpdate](https://docs.unity3d.com/ScriptReference/MonoBehaviour.LateUpdate.html)|1フレーム中の描画される直前に実行|
|[OnGUI](https://docs.unity3d.com/ja/current/ScriptReference/MonoBehaviour.OnGUI.html)|GUIが更新される度に実行|
|[OnCollisionEnter](https://docs.unity3d.com/ja/current/ScriptReference/Collider.OnCollisionEnter.html)|コライダの領域に衝突する度に実行|
|[OnTriggerEnter](https://docs.unity3d.com/ja/current/ScriptReference/Collider.OnTriggerEnter.html)|OnCollisionEnterに似ている（iSTriggerがアクティブな時）|
|[OnDestroy](https://docs.unity3d.com/ja/current/ScriptReference/MonoBehaviour.OnDestroy.html)|GameObjectが消える時に実行|

* マテリアルを変更する＝信号機を作る（188〜189頁）
    ```
    //Signal.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    //using UnityEditor; //AssetDatabase.LoadAssetAtPath()に必要

    public class Signal : MonoBehaviour {
        //publicの場合Inspector内で手作業で割当てる
        public GameObject _redCube;
        public GameObject _blueCube;
        public Material _blueMaterial;
        public Material _dakBlueMaterial;
        public Material _redMaterial;
        public Material _darkRedMaterial;

        //publicにしておくとInspectorで初期値の変更が可能（プレハブ化時に便利）
        private bool _onOff = false;

        void Start () {
            /* //変数をprivateにすると以下の処理が必要
            _redCube = GameObject.Find("RedCube"); //Hierarchy内で「GameObject」を探す
            _blueCube = GameObject.Find("BlueCube");
            _blueMaterial = AssetDatabase.LoadAssetAtPath("Assets/BlueMaterial.mat", typeof(Material)) as Material; //Assets内で「マテリアル」を探す
            _dakBlueMaterial = AssetDatabase.LoadAssetAtPath("Assets/DarkBlueMaterial.mat", typeof(Material)) as Material;
            _redMaterial = AssetDatabase.LoadAssetAtPath("Assets/RedMaterial.mat", typeof(Material)) as Material;
            _darkRedMaterial = AssetDatabase.LoadAssetAtPath("Assets/DarkRedMaterial.mat", typeof(Material)) as Material;
            */

            //最初の状態を作っておく
            _redCube.GetComponent<Renderer>().material = _darkRedMaterial;
            _blueCube.GetComponent<Renderer>().material = _blueMaterial;

            //3秒後から5秒間隔でSignalLoop()を繰返し実行
            InvokeRepeating("SignalLoop", 3.0f, 5.0f);
        }

        //InvokeRepeating()によって繰返し実行される処理
        void SignalLoop() {
            if (_onOff) {
                _redCube.GetComponent<Renderer>().material = _redMaterial;
                _blueCube.GetComponent<Renderer>().material = _dakBlueMaterial;
            } else {
                _redCube.GetComponent<Renderer>().material = _darkRedMaterial;
                _blueCube.GetComponent<Renderer>().material = _blueMaterial;
            }
            _onOff = !_onOff;
        }
    }
    ```

* [Transform](https://docs.unity3d.com/ja/current/ScriptReference/Transform.html)情報（全てのGameObjectに存在）

    |プロパティ名|記述方法|データ型|内容|
    |:--|:--|:--|:--|
    |[parent](https://docs.unity3d.com/jp/current/ScriptReference/Transform-parent.html)|GameObject.transform.parent|UnityEngine.Transform|親のGameObject（無い場合はNull）|
    |[root](https://docs.unity3d.com/jp/current/ScriptReference/Transform-root.html)|GameObject.transform.root|UnityEngine.Transform|最上位の親＝GameObject|
    |[childCount](https://docs.unity3d.com/jp/current/ScriptReference/Transform-childCount.html)|GameObject.transform.childCount|System.Int32|自分より下層のGameObjectの数（無い場合は0）|
    |[eulerAngles](https://docs.unity3d.com/ja/current/ScriptReference/Transform-eulerAngles.html)|GameObject.transform.eulerAngles|UnityEngine.Vector3|InspectorのRotation値 / (x,y,z) で出力|
    |[right](https://docs.unity3d.com/ja/current/ScriptReference/Transform-right.html)|GameObject.transform.right|UnityEngine.Vector3|赤軸 / (x,y,z) で出力|
    |[up](https://docs.unity3d.com/ja/current/ScriptReference/Transform-up.html)|GameObject.transform.up|UnityEngine.Vector3|緑軸 / (x,y,z) で出力|
    |[forward](https://docs.unity3d.com/jp/current/ScriptReference/Transform-forward.html)|GameObject.transform.forward|UnityEngine.Vector3|青軸 / (x,y,z) で出力|
    |[rotation](https://docs.unity3d.com/ja/current/ScriptReference/Transform-rotation.html)|GameObject.transform.rotation|UnityEngine.Quaternion|(x,x,x,x) で出力|
    |[localEulerAngles](https://docs.unity3d.com/ja/current/ScriptReference/Transform-localEulerAngles.html)|GameObject.transform.localEulerAngles|UnityEngine.Vector3|―|
    |[localPosition](https://docs.unity3d.com/ScriptReference/Transform-localPosition.html)|GameObject.transform.localPosition|UnityEngine.Vector3|―|
    |[localRotation](https://docs.unity3d.com/jp/460/ScriptReference/Transform-localRotation.html)|GameObject.transform.localRotation|UnityEngine.Quaternion|―|
    |[localScale](https://docs.unity3d.com/ja/current/ScriptReference/Transform-localScale.html)|GameObject.transform.localScale|UnityEngine.Vector3|―|
    |[lossyScale](https://docs.unity3d.com/jp/current/ScriptReference/Transform-lossyScale.html)|GameObject.transform.lossyScale|UnityEngine.Vector3|―|
    |[position](https://docs.unity3d.com/ja/current/ScriptReference/Transform-position.html)|GameObject.transform.position|UnityEngine.Vector3|―|
    |[localToWorldMatrix](https://docs.unity3d.com/jp/460/ScriptReference/Transform-localToWorldMatrix.html)|GameObject.transform.localToWorldMatrix|UnityEngine.Matrix4x4|―|
    |[worldToLocalMatrix](https://docs.unity3d.com/jp/current/ScriptReference/Transform-worldToLocalMatrix.html)|GameObject.transform.worldToLocalMatrix|UnityEngine.Matrix4x4|―|
    |[hasChanged](https://docs.unity3d.com/jp/current/ScriptReference/Transform-hasChanged.html)|GameObject.transform.hasChanged|System.Boolean|―|

* 継承される機能（全てのGameObjectに存在）

    |プロパティ名|記述方法|データ型|内容|
    |:--|:--|:--|:--|
    |[Animation](https://docs.unity3d.com/ja/current/ScriptReference/Animation.html)|GameObject.GetComponent&lt;Animation>()|UnityEngine.Animation|アタッチされているAnimation情報（無ければnull）|
    |[AudioSource](https://docs.unity3d.com/ja/current/ScriptReference/AudioSource.html)|GameObject.GetComponent&lt;AudioSource>()|UnityEngine.AudioSource|アタッチされているAudioSource情報（無ければnull）|
    |[Camera](https://docs.unity3d.com/ja/current/ScriptReference/GameObject-camera.html)|GameObject.GetComponent&lt;Camera>()|UnityEngine.Camera|アタッチされているCamera情報（無ければnull）|
    |[Collider](https://docs.unity3d.com/ja/current/ScriptReference/Collider.html)|GameObject.GetComponent&lt;Collider>()|UnityEngine.BoxCollider等|アタッチされているCollider情報|
    |[Collider2D](https://docs.unity3d.com/ja/current/ScriptReference/Collider2D.html)|GameObject.GetComponent&lt;Collider2D>()|UnityEngine.Collider2D|アタッチされているCollider2D情報|
    |[ConstantForce](https://docs.unity3d.com/ja/current/Manual/class-ConstantForce.html)|GameObject.GetComponent&lt;ConstantForce>()|UnityEngine.ConstantForce|アタッチされているConstantForce情報|
    |[GameObject](https://docs.unity3d.com/ja/current/ScriptReference/GameObject.html)|GameObject.gameObject|UnityEngine.GameObject|GameObject情報|
    |[GUIText](https://docs.unity3d.com/jp/current/Manual/class-GUIText.html)|GameObject.GetComponent&lt;GUIText>()|UnityEngine.GUIText|アタッチされているGUIText情報（旧UI）|
    |[GUITexture](https://docs.unity3d.com/jp/current/Manual/class-GUITexture.html)|GameObject.GetComponent&lt;GUITexture>()|UnityEngine.GUITexture|アタッチされているGUITexture情報（旧UI）|
    |[HingeJoint](https://docs.unity3d.com/ja/current/ScriptReference/HingeJoint.html)|GameObject.GetComponent&lt;HingeJoint>()|UnityEngine.HingeJoint|アタッチされているHingeJoint情報|
    |[Light](https://docs.unity3d.com/ja/current/Manual/class-Light.html)|GameObject.GetComponent&lt;Light>()|UnityEngine.Light|アタッチされているLight情報|
    |[NetworkView](https://docs.unity3d.com/ja/current/Manual/class-NetworkView.html)|GameObject.GetComponent&lt;NetworkView>()|UnityEngine.NetworkView|アタッチされているNetworkView情報|
    |[ParticleEmitter](https://docs.unity3d.com/ScriptReference/ParticleEmitter.html)|GameObject.GetComponent&lt;ParticleEmitter>()|UnityEngine.ParticleEmitter|アタッチされているParticleEmitter情報|
    |[ParticleSystem](https://docs.unity3d.com/ja/current/ScriptReference/ParticleSystem.html)|GameObject.GetComponent&lt;ParticleSystem>()|UnityEngine.ParticleSystem|アタッチされているParticleSystem情報|
    |[Renderer](https://docs.unity3d.com/jp/current/ScriptReference/GameObject-renderer.html)|GameObject.GetComponent&lt;Renderer>()|UnityEngine.MeshRenderer|アタッチされているRenderer情報|
    |[Rigidbody](https://docs.unity3d.com/ja/current/ScriptReference/Rigidbody.html)|GameObject.GetComponent&lt;Rigidbody>()|UnityEngine.Rigidbody|アタッチされているRigidbody情報|
    |[Rigidbody2D](https://docs.unity3d.com/ja/current/ScriptReference/Rigidbody2D.html)|GameObject.GetComponent&lt;Rigidbody2D>()|UnityEngine.Rigidbody2D|アタッチされているRigidbody2D情報|
    |[tag](https://docs.unity3d.com/jp/current/ScriptReference/GameObject-tag.html)|GameObject.tag|UnityEngine.String|GameObjectのタグ情報|
    |[Transform](https://docs.unity3d.com/ja/current/ScriptReference/Transform.html)|GameObject.transform|UnityEngine.Transform|GameObjectのタグ情報|
    |[HideFlags](https://docs.unity3d.com/ja/current/ScriptReference/HideFlags.html)|GameObject.hideFlags|UnityEngine.HideFlags|―|
    |[name](https://docs.unity3d.com/ja/current/ScriptReference/Object-name.html)|GameObject.name|UnityEngine.String|GameObjectの名前|

* 主なGameObject.transform.メソッド

    |メソッド|記述方法|戻り値|内容|記述例|
    |:--|:--|:--|:--|:--:|
    |[IsChildOf()](https://docs.unity3d.com/jp/460/ScriptReference/Transform.IsChildOf.html)|transform.IsChildOf()|bool|任意のGameObjectの子か調べる|―|
    |[LookAt()](https://unity3d.com/jp/learn/tutorials/topics/scripting/look)|transform.LookAt()|Void|任意のGameObjectの方向に向かせる|―|
    |[Rotate()](https://docs.unity3d.com/jp/530/ScriptReference/Transform.Rotate.html)|transform.Rotate()|Void|GameObjectを回転させる|[●](https://github.com/mubirou/Unity/tree/master/examples#%E3%83%9E%E3%82%A6%E3%82%B9%E3%83%9C%E3%82%BF%E3%83%B3%E3%81%A7%E5%9B%9E%E8%BB%A2)|
    |[Translate()](https://docs.unity3d.com/ja/530/ScriptReference/Transform.Translate.html)|transform.Translae()|Void|GameObjectを移動させる|[●](https://github.com/mubirou/Unity/tree/master/examples#%E3%82%AD%E3%83%BC%E3%81%A7%E5%8B%95%E3%81%8B%E3%81%99)|

* [Vector3](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)クラスの主な機能

    |プロパティ名|記述方法|内容|記述例|
    |:--|:--|:--|:--:|
    |[back](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.back|Vector3(0,0,-1)と同じ|―|
    |[down](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.down|Vector3(0,-1,0)と同じ|―|
    |[forward](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.forward|Vector3(0,0,1)と同じ|―|
    |[left](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.left|Vector3(-1,0,0)と同じ|―|
    |[one](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.one|Vector3(1,1,1)と同じ|―|
    |[right](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.right|Vector3(1,0,0)と同じ|―|
    |[up](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.up|Vector3(0,1,0)と同じ|―|
    |[zero](http://tech.pjin.jp/blog/2016/02/16/unity_vector3_1/)|Vector3.zero|Vector3(0,0,0)と同じ|―|

<a name="アニメーションとキャラクタ。"></a>
### 05 アニメーションとキャラクタ。</b>

* [Window]-[Animation] 上のFPSの値はあくまでキーフレームの設定用  
    ※低い値（6fps）でもカクカクしない
* [Blend Tree（ブレンドツリー）](https://docs.unity3d.com/ja/current/Manual/class-BlendTree.html) と [Animation Transition（アニメーション遷移）](https://docs.unity3d.com/ja/current/Manual/class-Transition.html) がある

<a name="GUIとAudio。"></a>
### 06 GUIとAudio。</b>

* 主な[GUI](https://docs.unity3d.com/ja/current/ScriptReference/GUI.html)

    |GUI名|内容|
    |:--|:--|
    |[Button](https://docs.unity3d.com/ja/current/ScriptReference/GUI.Button.html)|ボタン|
    |[Label](https://docs.unity3d.com/jp/460/ScriptReference/GUI.Label.html)|文字|
    |[Slider](https://github.com/mubirou/Unity/tree/master/examples#%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%80%E3%83%BC)|スライダー|

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年05月23日  
更新日：2018年07月18日


<a name="ユーザー設定"></a>
# <b>005 ユーザー設定</b>

初期設定では使いにくい設定を変更します。

1. [Edit]-[Preferences]-[Colors]
    * [General]-[Playmode tint] をダーク系（#666666FF等）にする……再生中であることを明確にする為

1. XXX

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年05月24日  
更新日：2018年06月30日

<a name="マウス操作"></a>
# <b>006 マウス操作</b>

|マウス操作|内容|DATE|
|:--|:--|:--:|
|[左ボタン]|オブジェクトの選択|2018-05-24|
|[Shift]+[左ボタン]|オブジェクトの選択の追加 / 選択の解除|2018-05-24|
|[ホイール回転]|視点のズームアップ･ズームダウン（画面中央を基準）|2018-05-24|
|[右ボタン]+[ドラッグ]|視点の回転|2018-05-24|
|[Shift]+[中ボタン]+[ドラッグ]|視点の自由移動|2018-05-24|

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS  
作成者：夢寐郎  
作成日：2018年05月24日  
更新日：2018年XX月XX日


<a name="出力"></a>
# <b>007 出力</b>

### プラットフォーム
[File]-[Build Settings] から選択  

|Platform|内容|
|:--|:--|
|PC, Mac & Linux Standalone|Windowsｍ･macOS･Linux用|
|iOS|iPhone･iPad用|
|Android|Android用|
|Tizen|スマホ等で使われるTizen OS用|
|WebGL|WebGL対応ブラウザ向け|
|Samsung TV|スマートテレビ用|
|Facebook|（Facebookアプリ用）|
|tvOS|Apple TV向け|
|Xbox One|Microsoft XBox One向け|
|PS Vista|SONY PlayStation Vita向け|
|PS4|SONY PlayStation 4向け|

### Linux Standaloneの場合（必要最低限の設定）  
1. プラットフォームの変更  
    ① [File]-[Build Settings]-[PC,Mac & Linux Standalone] を選択し [Switch Platform] を選択  
    ② [Add Open Scenes] を押して任意のシーンを選択  

1. カーソルの変更（タッチパネル用にカーソルをほとんど見えなくする場合）  
    ① [File]-[Build Settings]-[Play Settings] ボタンを押す  
    ② [Default Cursor] を1x1のPNGファイル（Inkscape等で作成）にする  

1. 起動時のダイアログ設定  
    ① [File]-[Build Settings]-[Play Settings] ボタンを押す  
    ② [Resolution and Presentation]-[Standalone Player Options]-[Display Resolution Dialog] を [Enabled] にする（初期値）  
    ※起動時に解像度設定のダイアログを表示したくない場合は「Disabled」  

1. Debug.Log()を出力させなくする  
    上記に引き続き [Use Player Log] の ✔ を外す

1. ビルド  
    ① [File]-[Build Settings]-[Build] を選択  
    ② 任意の場所に xxx..x86_64 ファイルを保存  
    ③ 任意の場所に生成されたアプリを選択し、再生されたら成功!!  

### Androidの場合（必要最低限の設定）
1. Android SDK（[Android Studio](https://ja.wikipedia.org/wiki/Android_Studio)）のインストール（[参考サイト](http://blog.tabolog.net/entry/2017/08/11/092821)）  
    ① [Edit]-[Preferences]-[External Tools] を選択  
    ② Android「SDK」の [Download] を選択  
    ③ [developer.android.com](https://developer.android.com/studio/#Other) の [DOWNLOAD ANDROID STUDIO] を選択  
    ④ ダウンロードされた android-studio-ide-XXX-linux.tar.gz を任意の場所に展開  
    ⑤ 端末で次の通りに実行（デスクトップに展開した場合）  
    ```
    $ /home/（ユーザ名）/デスクトップ/android-studio/bin/studio.sh
    ```
    ⑥ [Android Studio Setup Wizard] の指示に従いインストール  
    ⑦ /home/（ユーザ名）/Android/Sdk が作成されたのを確認  
    ⑧ Unityを起動し、[Edit]-[Preferences]-[External Tools] を選択  
    ⑨ Android「SDK」の [Browse] を選択し、上記のパス /home/（ユーザ名）/Android/Sdk を指定する  

1. [JDK](https://ja.wikipedia.org/wiki/Java_Development_Kit)のインストール  
    Android「JDK」のパスは /usr/lib/jvm/java-1.8.0-openjdk-amd64
    ※既にインストール済みの場合

1. [Android NDK](https://developer.android.com/ndk/guides/?hl=ja)のインストール  
    ① [Edit]-[Preferences]-[External Tools] を選択  
    ② Android「NDK」の [Download] を選択  
    ③ ダウンロードされた android-ndk-r13b-linux-x86_64.zip を任意の場所に展開  
    ④ Unityを起動し、[Edit]-[Preferences]-[External Tools] を選択  
    ⑤ Android「NDK」の [Browse] を選択し、展開したフォルダ android-ndk-r13b を指定  

1. プラットフォームの変更  
    ① [File]-[Build Settings]-[Android] を選択し [Switch Platform] を選択  
    ② [Add Open Scenes] を押して任意のシーンを選択  

1. アプリ名の設定  
    ① [File]-[Build Settings]-[Player Settings] ボタンを押す  
    ② [Product Name]（アプリ名）を設定（初期値はUnityのプロジェクト名）  
    ※この名前がAndroid端末上のアプリ名となる（数字から始まる名前でもOK）  
    ※下記の「アプリケーションID」の最後のドット以降と同じでなくてよい

1. Keystore（証明）ファイルの作成
    1. [File]-[Build Settings]-[Player Setting]-[Publishing Settings] ボタンを押す  
    1. [Keystore Manager] ボタンを選択すると [Keystore Manager] が現れます
    1. [Keystore...] ボタンを選択、[Create New]-[Anywhere] で保存先と名前（xxx.keystore）を決定

1. アプリケーションIDの登録  
    ① [File]-[Build Settings]-[Player Settings] ボタンを押す  
    ② [Other Settings]-[Identification] の [Package Name] を com.mubirou.app001 等（ユニーク値）にする  
    ※この値が違うと別のアプリとしてAndroid端末にインストールされる  
    ※数値から始まる名前は不可（要注意）

1. Android端末との接続  
    ① Android端末の [設定]-[システム]-[端末情報]-[ビルド番号] を7回タップ  
    ②「これで開発者になりました!」と表示されるのを確認
    ③ Android端末をPCに接続し [USB使用] ダイアログで [ファイルを転送] を選択

1. ビルド  
    ① [File]-[Build Settings]-[Build And Run] を選択  
    ② 任意の場所に xxx.apk ファイルを保存（アプリ名とは関係ない）  
    ③ Unityの左下に [Build Completed with a result of 'Succeeded'] と表示されたら成功  
    ④ 上記で指定した場所に xxx.apk が生成されたのを確認  
    ⑤ Android端末上に生成されたアプリを選択し、再生されたら成功!!  
    ※ xxx.apk の[ダウンロード](https://mubirou.github.io/Unity3D/introduction/apk/007.apk)（Android端末へのインストール用）  

実行環境：Unity 2019.1 Personal、Ubuntu 18.04 LTS、Android 9.0  
作成者：夢寐郎  
作成日：2018年06月20日  
更新日：2019年06月17日 [Keystoreファイルの作成] を Unity 2019.1 に対応


<a name="008"></a>
# <b>008 VideoPlayerコンポーネント（検証中）</b>

### 概要
* Unity 5.6（2017年3月リリース）より [VideoPlayerコンポーネント](https://docs.unity3d.com/ja/current/Manual/class-VideoPlayer.html) による動画ファイルの再生が可能
* Linuxの場合 [.webm](https://ja.wikipedia.org/wiki/WebM) または [.ogv](https://ja.wikipedia.org/wiki/Ogg) である必要がある（[.mp4](https://ja.wikipedia.org/wiki/MP4) は不可）（要検証）

### H264 / VP8 / VP9 について  
* 2010年、H.264ライセンス利用料の無料化を発表（それだけでは不十分との意見あり）
* 2011年、Google ChromeはH.264対応をやめWebM推進を発表
* 2011年、GoogleはHTML5ビデオでサポートするフォーマットとしてOgg TheoraとWebM（VP8）を選択
* AppleはVP8ではなくH.264を支持（品質的な理由）
* Ogg Theora（オッグ･シオラ）とはOn2VP3をベースに開発したビデオコーデック（音声コーデックにはOgg Vorbisを利用）
* VP8はGoogleに買収されたOn2テクノロジー社が開発したビデオコーデック
* VP9はVP8の後継（VP8の半分のビットレートで同等の画質を実現、H.265よりも効率的が目標）
* VP9はVP8より20％程度、CPUの使用率が高い
* VP9は動きにとても強い（対VP8、H.264比）
* UnityではVP8に対応（VP9は要調査）

### WebMへの変換
1. [Ubuntuソフトウェア] を起動し [Shotcut](https://www.shotcut.org/) をインストール＆起動  
    ※最新版（18.06.02）が必要な場合は[ここ](https://www.shotcut.org/download/)からダウンロード
1. [ファイルを開く] で任意の動画ファイルを開く
1. [ファイル]-[ビデオExport] を選択
1. [ストック] の中から [WebM] を選択（「WebM VP9」ではない）
1. [ビデオ] タブを選択し次の項目を確認
    * 解像度
    * アスペクトレイシオ
    * フレーム/秒（要調査：なぜか1000fpsになってしまう）
1. [コーデック] タブを選択し次の項目を確認
    * コーデック：libvpx ←VP8コーデックライブラリー
    * レートコントロール
    * ビットレート
1. [オーディオ] タブを選択し次の項目を確認
    * サンプルレート
    * コーデック：vorbis
    * レートコントロール
    * 品質
1. [ファイルをExport] ボタンを選んで xxx.webm の保存場所を指定して [保存]

### Unityで再生
1. Unityを起動しプロジェクトを作成
1. [File]-[Save Scene] でシーンを保存（名前は任意）
1. 上記で作成した xxx.webm をプロジェクトフォルダ内の [Assets] 内にコピー
1. [GameObject]-[3D Object]-[Quad] を選択
1. [Hierarchy] から [Quad] を選択し [Inspector] を確認
1. [Inspector]-[Transform] の [Scale] の値を適当に調整（映像の画角に合わせる）
    * X:8、Y:4.5、Z:1 など
1. 引き続き [Add Component] ボタンを押し [Video]-[Video Player] を選択
1. [Video Player] の [Video Clip] の [⦿] を選び、上記で作成した映像 xxx を選択
1. [▶] ボタンを押して [Quad] 上に映像ファイルが再生されたら成功
    * Linux Standalone では動作確認済み（タッチパネル等では利用可能）

### ビルド（Android）※現在調査中（下記の方法では動画ファイルが再生されず）
1. [出力](#出力)（Androidの場合）の処理を行う（まだビルドは行わない）
1. [File]-[Build Settings]-[Player Settings] ボタンを押す  
1. [Other Settings]-[Rendering] の [Multithreaded Rendering] の ✔ を外す
    ※再生時のコマ落ち防止用
1. [Build And Run] でビルド  
※上記に加えスクリプトの記述が必要の可能性あり

実行環境：Unity 2017.2 Personal、Ubuntu 16.04 LTS、Shotcut 18.03.06  
作成者：夢寐郎  
作成日：2018年06月26日  
更新日：2018年06月28日


<a name="逆引き大全"></a>
# <b>009 『Unity 2018 逆引き大全 300の極意』</b>

* 頁数は [『現場ですぐに使える! Unity 2018 逆引き大全 300の極意／薬師寺国安著』](https://amzn.to/2KuNW69) のページです。  
* .apk はAndroid端末へのインストール用です。  

|No.|内容|Tips番号|WebGL|.apk|project|参考サイト|更新日|
|:--|:--|:--:|:--:|:--:|:--:|:--:|:--:|
|001|[Unityのエディション](#Unityのエディション)|004|－|－|－|[●](https://store.unity.com/ja)|2018-06-29|
|002|[Asset Store保存場所](#AssetStore保存場所)|007|－|－|－|－|2018-06-29|
|003|[Editorの設定](#Editorの設定)|008|－|－|－|－|2018-12-10|
|004|[マテリアルに画像を指定](#マテリアルに画像を指定)|022･023|－|[●](https://mubirou.github.io/Unity3D/introduction/apk/009_004.apk)|－|－|2018-06-29|
|005|[空の背景の変更](#空の背景の変更)|028|－|－|－|－|2018-07-01|
|006|[床を鏡のようにする](#床を鏡のようにする)|031|－|[●](https://mubirou.github.io/Unity3D/introduction/apk/009_006.apk)|－|[●](http://corevale.com/unity/923)|2018-07-02|
|007|[Planeに動画を表示](#Planeに動画を表示)|032|－|－|－|－|2018-07-02|
|008|[ボールに重力を持たせる](#ボールに重力を持たせる)|030･033|－|－|－|－|2018-07-02|
|009|[オブジェクトの透明化](#オブジェクトの透明化)|033|－|－|－|－|2018-07-02|
|010|[クリックした位置にPrefabを表示](#クリックした位置にPrefabを表示)|034|－|[●](https://mubirou.github.io/Unity3D/introduction/apk/009_010.apk)|－|－|2018-07-03|
|011|[MouseOverで色を変える](#MouseOverで色を変える)|035|－|[●](https://mubirou.github.io/Unity3D/introduction/apk/009_011.apk)|－|－|2018-07-04|
|012|[オブジェクトをクリックで落下](#オブジェクトをクリックで落下)|036|－|[●](https://mubirou.github.io/Unity3D/introduction/apk/009_012.apk)|－|－|2018-07-04|

<a name="Unityのエディション"></a>
### 001 Unityのエディション

1. Personal（無料）……起動時の「Made with unity」ロゴを非表示できない
1. Plus（4,200円/月）……Apple Store製品20％割引（クリエイター向き）
1. Pro（15,000円/月）……Apple Store製品20％割引（プロ志向）

<a name="AssetStore保存場所"></a>
### 002 Asset Store保存場所（Ubuntuの場合）
```
ホーム/.local/share/unity3d/Asset Store-5.x
```
一度ダウンロードしてインポートしたものは上記の場所に保存され、次回からは「インポート」と表示される

<a name="Editorの設定"></a>
### 003 Editorの設定（Visual Studio Codeの場合）
[Edit]-[Preferences]-[External Tools]-[External Script Editor] で [Browse] を選び以下のパスを指定する
```
/usr/share/code/code
```
従来付属していた「MonoDevelop」はサポートされない（Unity 2018.1〜）

<a name="マテリアルに画像を指定"></a>
### 004 マテリアルに画像を指定

1. デスクトップ等にある画像ファイル（.png .jpg）を [Project]-[Assets] にドラッグ＆ドロップ
1. [Scene] 上のマテリアルを適用したいオブジェクトに上記の画像をドラッグ＆ドロップ

<a name="空の背景の変更"></a>
### 005 空の背景の変更

1. [Window]-[Asset Store] から「Wispy SkyBox」をダウンロード＆インポート
1. [Hierarchy]-[Main Camera] を選択し [Inspector]-[Add Component]-[Rendering]-[Skybox] を追加
1. [Inspector]-[Skybox]-[Custom Skybox] の ⦿ を選び、任意の空の背景を選択

<a name="床を鏡のようにする"></a>
### 006 床を鏡のようにする

1. [Assets]-[Materials] で右クリック → [Create]-[Material] を選択（名前は任意）
1. [Inspector] で次の通りに設定  
    * Metallic : 1
    * Smoothness : 1
1. 床（Plane）に上記のマテリアルをドラッグ
1. [GameObject]-[Create Empty] で空のGameObjectを作成（名前は任意）
1. [Inscpector]-[Add Component] から「Reflection Prob」を検索して追加
1. [Inspector]-[Reflection Probe] で次の通りに設定
    * Type : Realtime
    * Refresh Mode : Every frame
    * Time Slicing : All faces at one（初期値）
    * Box Projection : ✔
    * Resolution : 512
    * Clear Flags : Solid Color
1. [Hierarchy]-[Main Camera] と床の [Inspector]-[Transform]-[Position] の値を確認
1. [Reflection Probe] を追加した空のGameObjectの [Inspector]-[Transform]-[Position] の値を次の通りにする（[Main Camera] の [Potision] の値が「X:0」「Y:2.5」「Z:-10」、床が「X:0」「Y:0」「Z:0」の場合）
    * x : 0
    * Y : -2.5（この値だけ負の値にする）
    * Z : -10
※Androidアプリでは鏡内のアニメーションが動作せず（要検証）

<a name="Planeに動画を表示"></a>
### 007 Planeに動画を表示

1. [Hierarchy]-[Create]-[3D Object]-[Plane] を選択
1. [Inscpector]-[Transform]-[Rotation] を次の通りに設定
    * X : 90
    * Y : 0
    * Z : -180 
1. [Shotcut](https://www.shotcut.org/) 等で作成した [.webm](https://ja.wikipedia.org/wiki/WebM) ファイルを、プロジェクトの [Assets] フォルダに保存
1. 上記で作成した [Plane] の [Inspector]-[Add Component]-[Video Player] を選択
1. [Inspector]-[Video Player]-[Video Clip] の ⦿ を選び、上記の映像を選択

<a name="ボールに重力を持たせる"></a>
### 008 ボールに重力を持たせる
1. [GameObject]-[3D Object]-[Sphere] でボールを作成
1. 同様に [Cube] を使って障害物を作成
1. [Sphere]-[Inspector]-[Add Component]-[Physics]-[Rigidbody] を選択
1. 再生ボタンを押すとボールが落下（障害物にぶつかると変化する）

<a name="オブジェクトの透明化"></a>
### 009 オブジェクトの透明化

1. [Project]-[Assets] を選択し右クリック
1. [Create]-[Folder] でフォルダを作成（名前は「Materials」とする）
1. 作成した [Materials] フォルダを選び右クリック
1. [Create]-[Material] でマテリアルを作成（名前は任意）
1. 作成したマテリアルの [Inspector] の値を次の通りにする
    * Rendering Mode : Fade
    * Albedo : A（Apha値）を0にする

※透明化されただけで存在はしている（衝突判定は有効）

<a name="クリックした位置にPrefabを表示"></a>
### 010 クリックした位置にPrefabを表示

* 「Prefab（プレハブ）」とは、オブジェクトを複製する場合に役立つ機能で、オブジェクトとそのコンポーネントやプロパティを一つに格納するものです
1. オブジェクト（Sphere）の作成  
    [GameObject]-[3D Object]-[Sphere] を選択  
1. オブジェクトのPrefab化  
    [Hierarchy] に表示される上記のオブジェクトを [Project]-[Assets] フォルダ内にドラッグ＆ドロップ  
    ※[Hierarchy] 内の上記のオブジェクトの文字色が青系に変わります  
    ※[Hierarchy] 内の上記のオブジェクトはここでは消します  
1. 空のゲームオブジェクトを作成  
    ① [GameObject]-[Create Empty] を選択  
    ② [Inspector] ウィンドウで、名前を "GameObject" から "God" に変更  
1. C#ファイルの作成  
    ① 上記の空のGameObject（God）を選択  
    ② [Inspector]-[Add Component]-[Net Script] を選択  
    ③ 名前を "NewBehaviourScript" から "CreateSphereScript" に変更  
1. C#の記述  
    ① [Project]-[Assets] 内の [CreateSphereScript]（C#）をダブルクリック  
    ※[Editorの設定](#Editorの設定)を設定していれば外部エディタが起動します  
    ② 次のように書き換えて保存  
    ```
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class CreateSphereScript : MonoBehaviour {
        public GameObject _prefab;
        private Vector3 _mousePosition;

        void Update () {
            if (Input.GetMouseButton(0)) {
                _mousePosition = Input.mousePosition;
                _mousePosition.z = 5f;
                Instantiate(
                    _prefab,
                    Camera.main.ScreenToWorldPoint(_mousePosition),
                    _prefab.transform.rotation
                );
            }
        }
    }
    ```
1. public変数（_prefab）とPrefabをリンク  
    ① [Hierarycy]-[God] を選択  
    ② [Inspector]-[CreateSphereScript（Script）] に [Prefab] プロパティが追加されているのを確認  
    ③ ⦿を選び上記でPrefab化したオブジェクト（Sphere）を選択  
1. 実行  
    再生ボタンで実行し、クリックしたところにSphereが次々作成されたら成功

<a name="MouseOverで色を変える"></a>
### 011 MouseOverで色を変える

1. [GameObject]-[3D Object]-[Sphere] で球体を作成（名前は "Sphere01" に変更）
1. [Hierarchy]-[Sphere]-[Inspector]-[Add Component]-[Net Script] で名前は "ChangeColorScript" のC#ファイルを作成
1. [Project]-[Assets]-[ChangeColorScript]（C#）をダブルクリック
1. Visual Studio Codeなどのエディタで次の通りに書き換える
    ```
    //ChangeColorScript.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class ChangeColorScript : MonoBehaviour {
        private GameObject _sphere;

        void Start() {
            _sphere = GameObject.Find("Sphere01");
        }
        
        void OnMouseOver() {
            Debug.Log(_sphere);
            _sphere.GetComponent<Renderer>().material.color = Color.red;
        }

        void OnMouseExit() {
            _sphere.GetComponent<Renderer>().material.color = Color.blue;
        }
    }
    ```
1. 実行すると球体の上にマウスカーソルを乗せると赤に変わり、外すと青になれば成功  
    ※Androidアプリでも有効

<a name="オブジェクトをクリックで落下"></a>
### 012 オブジェクトをクリックで落下

1. 球体（Sphere）の [Inspector]-[Add Component]-[Physics]-[Rigidbody] を追加
1. [Inspector]-[Rigidbody]-[Use Gravity] の ✔ を外す
1. [Hierarchy]-[Sphere]-[Inspector]-[Add Componet]-[New Script] でC#ファイルを作成（名前は "DropSphereScript"）
1. 次の通りにコードを変更
    ```
    //DropSphereScript.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class DropSphereScript : MonoBehaviour {
        void Update () {
            if (Input.GetMouseButtonUp(0)) {
                GetComponent<Rigidbody>().useGravity = true;
            }
        }
    }
    ```

※上記の例の場合、オブジェクト以外をクリックしても落下する

実行環境：Unity 2017.2 Personal、Ubuntu 18.0.4.1 LTS、Android 8.0  
作成者：夢寐郎  
作成日：2018年06月28日  
更新日：2018年XX月XX日 Ubuntu 16.04.4 LTS を 18.0.4.1 LTS にアップデート
更新日：2018年07月04日


<a name="010"></a>
# <b>010 Analog Watch</b>

1. Unity（C#）で時刻を取得してみる（空のGameObjectにアタッチ）
    ```
    //Main.cs
    using UnityEngine;
    using System; //DateTimeに必要

    public class Main : MonoBehaviour {
        void Update () {
            DateTime _now = DateTime.Now; //現在の日時情報を取得

            int _hour = _now.Hour; //0〜23（時）
            int _minute = _now.Minute; //0〜59（分）
            int _second = _now.Second; //0〜59（秒）

            Debug.Log(_hour + "時" + _minute + "分" + _second + "秒"); //Consoleに出力
        }
    }
    ```

1. Blenderで針をモデリングする（ProjectのAssetsフォルダに保存）
    * 秒針（[secondHand.blend](https://mubirou.github.io/Unity3D/introduction/blend/secondHand.blend))
    * 分針（[minuteHand.blend](https://mubirou.github.io/Unity3D/introduction/blend/minuteHand.blend))
    * 時針（[hourHand.blend](https://mubirou.github.io/Unity3D/introduction/blend/hourHand.blend)）

1. Sceneビューに針を配置（Positionのみ変更／秒針が一番上）

    |オブジェクト名|X|Y|Z|
    |:--|:--|:--:|:--:|
    |secondHand|0|**0.55**|0|
    |minuteHand|0|**0.3**|0|
    |hourHand|0|0|0|

    ※Materialを使って秒針だけ赤にする（任意）

1. MainCameraの位置を変更（真上から見下ろす状態にする）

    |属性|X|Y|Z|
    |:--|:--|:--:|:--:|
    |Position|0|**35**（任意）|**0**|
    |Rotation|**90**|0|0|

1. 上記のプログラムを書き換える（プログラムの完成）
    ```
    //Main.cs
    using UnityEngine;
    using System; //DateTimeに必要

    public class Main : MonoBehaviour {
        //変数（ターゲットのGameObjectの参照）宣言
        private GameObject _seconHand;
        private GameObject _minuteHand;
        private GameObject _hourHand;

        void Start () {
            //シーンの中から任意のGameObjectを探す
            _seconHand = GameObject.Find("secondHand");
            _minuteHand = GameObject.Find("minuteHand");
            _hourHand = GameObject.Find("hourHand");
        }

        void Update () {
            //現在の日時情報を取得
            DateTime _now = DateTime.Now;

            //時針（1分毎に更新）
            float _hourRotation = _now.Hour * 30 + (float)(_now.Minute * 0.5);
            _hourHand.transform.eulerAngles = new Vector3(0, _hourRotation, 0);

            //分針（1秒毎に更新）
            float _minuteRotation = _now.Minute * 6 + (float)_now.Second / 60 * 6;
            _minuteHand.transform.eulerAngles = new Vector3(0, _minuteRotation, 0);

            //秒針（1秒毎に更新）
            int _secondRotation = _now.Second * 6; //0〜360
            _seconHand.transform.eulerAngles = new Vector3(0, _secondRotation, 0);
        }
    }
    ```

1. Blenderで文字盤（[dial.blend](https://mubirou.github.io/Unity3D/introduction/blend/secondHand.blend)）をモデリングする（ProjectのAssetsフォルダに保存）

1. [出力](#出力)の設定

1. 影が出ない問題の解決（Android端末）  
    [Edit]-[Project Settings]-[Quality] でAndroidの「Levels」の「Default」を「Medium」→「Ultra」に変更

1. 影のジャギーを解決（Android端末）  
    [Edit]-[Project Settings]-[Quality]-[Shadow Distance] を「150」→「40」程度に変更

1. 縦持ち限定にする（Android端末）  
    [Edit]-[Project Settings]-[Player]-[Resolution and Presentation]-[Default Orientation] の値を「Auto Rotation」→「Portrait」に変更

完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/010.zip)

実行環境：Unity 2017.2 Personal、Ubuntu 18.0.4.1 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年09月20日  
更新日：2018年09月21日


<a name="011"></a>
# <b>011 Drop Hole</b>

1. [Inkscape](https://inkscape.org)で平面素材（橋）を作成
（[bridge.svg](https://mubirou.github.io/Unity3D/introduction/svg/bridge.svg)）

1. Blenderで上記を読込み加工（[floor.blend](https://mubirou.github.io/Unity3D/introduction/blend/floor.blend)）
    * [ファイル]-[インポート]-[Scalable Vector Graphics（.svg）]
    * [編集モード]-[拡大縮小]
    * [マテリアル]の変更
    * [厚み付け]
    * [カーブからメッシュに変換]
    * [オブジェクトモード]-[立方体]の作成し加工
    * 上記を[統合]
    * [ブーリアン]を使い[円柱]でゴール地点に穴を空ける
    * [マテリアル]を使い配色
    * [Camera]、[Lamp]等の不要物を削除
    * [ファイル]-[エクスポート]-[**FBX（.fbx）**]で出力（[floor.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/floor.fbx)）

1. Unityで上記を読込み作業
    * プロジェクトの[Assets]フォルダに上記のfbxファイルを保存
    * Sceneビューに針を配置し調整（任意）
    * [Gameビュー]のサイズを9:16（1080x1920）にする
    * MainCameraの位置を変更（真上から見下ろす状態にする）  

        |属性|X|Y|Z|
        |:--|:--|:--:|:--:|
        |Position|0|**15**（要調整）|****|
        |Rotation|**90**|0|0|

1. ここで[出力](#出力)して確認

1. 縦持ち限定にする（Android端末）  
    * [Edit]-[Project Settings]-[Player]-[Resolution and Presentation]-[Orientation]-[Default Orientation] の値を"Portrait"に変更（初期値は"Auto Rotation"）

1. 影が出ない問題の解決（Android端末）  
    * [Edit]-[Project Settings]-[Quality] でAndroidの「Levels」の「Default」を"Ultra"に変更（初期値は"Medium"）

1. 影のジャギーを解決（Android端末）  
    * [Edit]-[Project Settings]-[Quality]-[Shadow Distance] を"20"程度に変更（初期値は"150"）

1. ボールを配置し物理的に落下させる
    * [Hierarchy]-[Create]-[3D Object]-[Sphere]
    * [Inspector]-[Transform]-[Scale]を調整
    * [Inspector]-[Add Component]-[Physics]-[**Rigidbody**]  
    ※再生させてテスト（床は通過してしまう）

1. 床に[コライダー](https://docs.unity3d.com/jp/460/Manual/CollidersOverview.html)（衝突判定領域）を設定
    * 床のオブジェクトの[Inspector]-[Add Component]-[Physics]-[**Mesh Collider**]  
    ※再生させてテスト（複雑な形状の床にも衝突する）

1. ボールの重さを変更する（1個の場合変化が分かりにくい）
    * [Inspector]-[Rigidbody]-[**Mass**]の値を変更する（初期値は1）

1. ボールをバウンドさせる
    * [Project]-[Create]-[**Physic Material**]を選択（名前をBallにする＝任意）
    * 上記の[Inspector]-[**Bounciness**]の値を0.8等にする（初期値は0）
    * ボールの[Inspector]-[Sphere]-[Material]へドラッグ＆ドロップ

1. 加速度センサーの利用
    * [Object]-[Create Empty]で空のGameObjectを作成（名前は任意）
    * [Assets]-[Create]-[C# Script]で名前は"AccelerometerController"（加速度センサーコントローラー）として以下の通りに記述する
    ```
    //AccelerometerController.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class AccelerometerController : MonoBehaviour {
        const float _gravity = 9.81f * 3; //重力加速度度（微調整）
        
        void Update () {
            Vector3 _vector = new Vector3(); //重力ベクトルの初期化

            _vector.x = Input.acceleration.x;
            _vector.z = Input.acceleration.y;
            _vector.y = Input.acceleration.z;

            Physics.gravity = _gravity * _vector.normalized;
        }
    }
    ```
    * 上記の空のGameObject（AccelerometerController）にC#（"AccelerometerController"）をドラッグ＆ドロップ

1. 水面を作成
    * [Hierarchy]-[Create]-[Plane]で作成
    * [Inspector]でサイズ･位置を修正

        |属性|X|Y|Z|
        |:--|:--|:--:|:--:|
        |Position|0|**-0.2**（要調整）|****|
        |Scale|**0.9（要調整）**|1|**1.7（要調整）**|
    
    * [Project]-[Create]-[Material]で作成（名前は"Blue"）、[Albedo]で色を指定し、上記のPlaneにドラッグ＆ドロップ
    * [Inspector]-[MEsh Collider]を無効にする（✔を外す）

1. ボールの位置の操作
* [Object]-[Create Empty]で空のGameObjectを作成（名前は任意）
    * [Assets]-[Create]-[C# Script]で名前は"BallController"にして次の通りに記述
    ```
    //BallController.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class BallController : MonoBehaviour {
        private GameObject _ball; //ターゲットのGameObjectの参照
        private float _originX;
        private float _originY;
        private float _originZ;

        void Start () {
            _ball = GameObject.Find("Ball"); //シーンの中から任意のGameObjectを探す
            _originX = _ball.transform.position.x;
            _originY = _ball.transform.position.y;
            _originZ = _ball.transform.position.z;
        }
        
        void Update () {
            //ボールが水面下に落ちたら最初の位置に再登場させる
            if (_ball.transform.position.y < -1) {
                Vector3 _pos = _ball.transform.position;
                _pos.x = _originX;
                _pos.y = _originY;
                _pos.z = _originZ;
                _ball.transform.position = _pos;
            }
        }
    }
    ```
    * 上記の空のGameObject（BallController）にC#（"BallController"）をドラッグ＆ドロップ

1. [出力](#出力)して確認

完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/011.zip)

実行環境：Unity 2017.2 Personal、Ubuntu 18.0.4.1 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年10月03日  


<a name="012"></a>
# <b>012 Stop Watch</b>

1. 下準備（とりあえず出力までやってみる）
    * シーンの保存：[File]-[Save Scene]
    * 画面サイズの設定：[Gameビュー]で9:16（1080x1920）にする
    * [出力](#出力)の各種設定を行いビルドしてみる
    * 縦持ち限定にする：[Edit]-[Project Settings]-[Player]-[Resolution and Presentation]-[Default Orientation] の値を"Portrait"に変更

1. テキストの表示
    * uGUIのTextを配置：[GameObject]-[UI]-[Text]
    * オブジェクト名を変更：[Inspector]の"Text"→"TextMessage"に変更
    * フォントを用意：プロジェクトフォルダ-[Assets]にTrueType（.ttf）またはOpenType（.otf）ファイルを置く
    * フォントを変更：[Hierarchy]-[Canvas]-[Text]-[Inspector]-[Text]-[Charactor]で上記のフォントを選択
    * テキスト内容を変更：[Hierarchy]-[Canvas]-[Text]-[Inspector]-[Text]-[Text]を"New Text"→"00:00:000"に変更
    * Canvasのスケール変更：[Hierarchy]-[Canvas]-[Inspector]-[CanvasScaler（Script）]-[ScaleFactor]を"1"→"7"に変更  
    （__テキストがボケるのを回避するため__）
    * 位置･サイズを変更：[Hierarchy]-[Canvas]-[Text]-[Inspector]-[RectTransform]

        |PosX|PosY|PosZ|
        |:--|:--|:--:|
        |**0**|**33.5**|0|

        |Width|Height|
        |:--|:--|
        |**124**|30|
    
    * フォントサイズの変更：[Canvas]-[Text]-[Inspector]-[Text]-[FontSize]を"14"→"24"に変更

    * フォントカラーの変更：[Canvas]-[Text]-[Inspector]-[Text]-[Color]を変更
    * 左寄せにする：[Hierarchy]-[Canvas]-[StartStopButton]-[Inspector]-[Text]-[Paragraph]-[Alignment]を左寄せにする

1. START/STOPボタンの表示
    * uGUIのButtonを配置：[GameObject]-[UI]-[Button]
    * オブジェクト名を変更：[Inspector]の"Button"→"StartStopButton"に変更
    * 表示文字の変更：[Hierarchy]-[Canvas]-[StartStopButton]-[Text]-[Inspector]-[Text]-[Text]を"Button"→"START"に変更
    * 位置を変更：[Hierarchy]-[Canvas]-[StartStopButton]-[Inspector]

        |PosX|PosY|PosZ|
        |:--|:--|:--:|
        |**0**|**-50**|0|

    * サイズを調整：[Hierarchy]-[Canvas]-[StartStopButton]-[Inspector]-[Scale]を調整

1. CLEARボタンの表示
    * 上記のボタンをコピー（[Edit]-[Copy]）＆ペースト（[Edit]-[Paste]）
    * オブジェクト名を変更：[Inspector]の"StartStopButton (1)"→"ClearButton"に変更
    * 位置を変更：[Hierarchy]-[Canvas]-[ClearButton]-[Inspector]

        |PosX|PosY|PosZ|
        |:--|:--|:--:|
        |**0**|**-88**|0|
    
    * 表示文字の変更：[Hierarchy]-[Canvas]-[ClearButton]-[Text]-[Inspector]-[Text]-[Text]を"START"→"CLEAR"に変更

1. START/STOP用スクリプトの記述
    * [Assets]-[Create]-[C# Script]で名前は"StartStopButton"にして次の通りに記述し、[Hierarchy]-[Canvas]-[StartStopButton]-[Inspector]にドラッグ＆ドロップ
    ```
    //StartStopButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    using UnityEngine.UI; //Textに必要
    using System; //DateTimeに必要


    public class StartStopButton : MonoBehaviour {
        private Text _textMessage;
        private GameObject _clearButton;
        private long _startTime;
        private bool _isStart = false;
        private long _currentTime;
        private long _lapTime = 0;

        // Use this for initialization
        void Start () {
            _textMessage = GameObject.Find("TextMessage").GetComponentInChildren<Text>();
            _clearButton = GameObject.Find("ClearButton");
        }
        
        // Update is called once per frame
        void Update () {
            if (_isStart) {
                //経過時間（100ナノ秒単位）最大35999990000まで=約60分
                _currentTime = _lapTime + DateTime.Now.Ticks - _startTime; 

                //ミリ秒（000〜999）を取得
                float _tmp = _currentTime/1000;
                long _tmpLong = (long)(Math.Round(_tmp/10) % 1000);
                string _millisec;
                if (_tmpLong < 10) {
                    _millisec = "00" + _tmpLong.ToString();
                } else if (_tmpLong < 100) {
                    _millisec = "0" + _tmpLong.ToString();
                } else {
                    _millisec = _tmpLong.ToString();
                }

                //秒（0〜59）を取得
                _tmp = _currentTime/100000;
                _tmpLong = (long)(Math.Floor(_tmp/100) % 60);
                string _second;
                if (_tmpLong < 10) {
                    _second = "0" + _tmpLong.ToString();
                } else {
                    _second = _tmpLong.ToString();
                }

                //分（0〜59）を取得
                _tmp = _currentTime/10000000;
                _tmpLong = (long)(Math.Floor(_tmp/60));
                if (60 <= _tmpLong) _tmpLong %= 60;
                string _minute;
                if (_tmpLong < 10) {
                    _minute = "0" + _tmpLong.ToString();
                } else {
                    _minute = _tmpLong.ToString();
                }

                _textMessage.text = _minute + ":" + _second + ":" + _millisec;
            }
        }

        public void OnClick() {
            foreach(Transform _child in this.transform) {
                if(_child.name == "Text") {
                    if (_child.GetComponent<Text>().text == "START") {
                        _startTime = DateTime.Now.Ticks; //100ナノ秒単位
                        _child.GetComponent<Text>().text = "STOP";
                        _isStart = true;
                        //他のGameObjectにアタッチされたclassのメソッドを実行
                        _clearButton.GetComponent<ClearButton>().Hide();

                    } else if (_child.GetComponent<Text>().text == "STOP") {
                        _child.GetComponent<Text>().text = "START";
                        _isStart = false;
                        _lapTime = _currentTime;
                        //他のGameObjectにアタッチされたclassのメソッドを実行
                        _clearButton.GetComponent<ClearButton>().Show();
                    }
                }
            }
        }

        public void ResetTime() { //外部からアクセス
            _lapTime = 0;
        }
    }
    ```

    * OnClick()メソッドの有効化：[Hierarchy]-[Canvas]-[StartStopButton]-[Inspector]-[Button]-[OnClick()]の[+]を選択し、[None（Object）]→[**Sceneタブ**]-[StartStopButton]に変更し、[NoFunction]→[StartStopButton]-[OnClick]を選択（StartStopButton.OnClickになる）  
    （__非常にわかりにくい操作__）

1. CLEAR用スクリプトの記述
    * [Assets]-[Create]-[C# Script]で名前は"ClearButton"にして次の通りに記述し、[Hierarchy]-[Canvas]-[ClearButton]-[Inspector]にドラッグ＆ドロップ
    ```
    //ClearButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    using UnityEngine.UI; //Buttonに必要

    public class ClearButton : MonoBehaviour {
        private Text _textMessage;
        private GameObject _startStopButton;

        void Start () {
            _textMessage = GameObject.Find("TextMessage").GetComponentInChildren<Text>();
            _startStopButton = GameObject.Find("StartStopButton");
        }

        public void OnClick() {
            //他のGameObjectにアタッチされたclassのメソッドを実行
            _startStopButton.GetComponent<StartStopButton>().ResetTime();
            _textMessage.text = "00:00:000";
        }

        public void Show() { //カスタムメソッド（外部からアクセス）
            this.GetComponent<Button>().interactable = true;
        }

        public void Hide() { //カスタムメソッド（外部からアクセス）
            this.GetComponent<Button>().interactable = false;
        }
    }
    ```

    * OnClick()メソッドの有効化：[Hierarchy]-[Canvas]-[ClearButton]-[Inspector]-[Button]-[OnClick()]の[+]を選択し、[None（Object）]→[ClearButton]に変更し、[NoFunction]→[ClearButton]-[OnClick]を選択（ClearButton.OnClickになる）  
    （__非常にわかりにくい操作__）

1. [再生]ボタンを押すか、[出力](#出力)して確認

完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/012.zip)

実行環境：Unity 2017.2 Personal、Ubuntu 18.0.4.1 LTS、Android 8.0  
作成者：夢寐郎  
作成日：2018年10月15日  


<a name="013"></a>
# <b>013 Mouse Stalker</b>

1. Blenderで適当なオブジェクトを作成（[piece.blend](https://mubirou.github.io/Unity3D/introduction/blend/piece.blend)）
    * [ファイル]-[エクスポート]-[**FBX（.fbx）**]で出力（[piece.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/piece.fbx)）

1. Unityで上記を読込み作業
    * プロジェクトの[Assets]フォルダに上記のfbxファイルを保存
    * [Hierarchy]に上記のオブジェクト（piece）をドラッグ

1. カメラの位置の調整

    * [MainCamera]-[Inspector]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |0|**0**|**-30**|

1. スクリプトの記述
    * [Object]-[CreateEmpty]で空のGameObjectを作成（名前は任意）
    * [Assets]-[Create]-[C# Script]で名前は"Main"とする
    * 上記の空のGameObjectの[Inspector]に上記のC#（Main.cs）をドラッグ
    * C#（Main.cs）を以下の通りに変更する
    ```
    //Main.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class Main : MonoBehaviour {
        private GameObject _piece0;
        private UnityEngine.Camera _mainCamera;
        private List<GameObject> _pieceList; //動的配列の宣言
        private uint _pieceNum = 30; //700個は可能

        void Start () {
            _piece0 = GameObject.Find("piece");
            _mainCamera = Camera.main.GetComponent<Camera>();

            _pieceList = new List<GameObject>(); //空の動的配列の作成

            _pieceList.Add(_piece0); //先頭のpieceを動的配列に格納

            //2つ目以降のpieceを動的配列に格納
            for (int i=1; i<=_pieceNum; i++) { //iはfor文内のみ有効（1,2,...,_pieceNum）
                GameObject _thePiece = Instantiate(
                    _piece0,
                    _piece0.transform.position,
                    _piece0.transform.rotation
                );
                _pieceList.Add(_thePiece);
            }

            //先頭を見えなくする
            _piece0.SetActive (false);
        }

        void Update () {
            //マウスの位置を取得し、スクリーン座標→ワールド座標に変換
            Vector3 _mousePos = Input.mousePosition;
            _mousePos.z = 30f; //マウスの位置をカメラから遠ざける
            Vector3 _mouseWoldPos = _mainCamera.ScreenToWorldPoint(_mousePos);
            _piece0.transform.position = _mouseWoldPos;

            for (int i=1; i<=_pieceNum; i++) { //iはfor文内のみ有効（1,2,...,_pieceNum）
                GameObject _thePiece = _pieceList[i];
                GameObject _frontPiece = _pieceList[i-1];
                
                float _disX = _frontPiece.transform.position.x - _thePiece.transform.position.x;
                float _disY = _frontPiece.transform.position.y - _thePiece.transform.position.y;
                float _disZ = _frontPiece.transform.position.z - _thePiece.transform.position.z;

                //角度
                _thePiece.transform.LookAt(_frontPiece.transform);

                //追従させる（角度付きの場合）
                Vector3 _thePos = _thePiece.transform.position;
                _thePos.x += _disX/8;
                _thePos.y += _disY/8;
                _thePos.z += _disZ/8+0.4f;
                _thePiece.transform.position = _thePos;

                //追従させる（角度固定の場合）
                //Vector3 _addPoint = new Vector3(_disX/4, _disY/4, _disZ/5+0.4f);
                //_thePiece.transform.Translate(_addPoint);
            }
        }
    }
    ```

1. [再生]ボタンを押すか、[出力](#出力)して確認

完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/013.zip)

実行環境：Unity 2017.2 Personal、Ubuntu 18.0.4.1 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年10月24日  


<a name="014"></a>
# <b>014 UFO Shooting</b>

1. BlenderでUFOを作成（[ufo.blend](https://mubirou.github.io/Unity3D/introduction/blend/ufo.blend)）
    * [ファイル]-[エクスポート]-[**FBX（.fbx）**]で出力（
    [piece.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/ufo.fbx)）

1. Blenderでミサイルを作成（[missile.blend](https://mubirou.github.io/Unity3D/introduction/blend/missile.blend)）
    * [ファイル]-[エクスポート]-[**FBX（.fbx）**]で出力（[piece.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/missile.fbx)）

1. Unityで上記を読込み作業
    * プロジェクトの[Assets]フォルダに上記のfbxファイルを保存
    * プロジェクトの[Assets]フォルダ内に[blender]フォルダを作成し、上記のblenderファイルを保存  
    （※本来blenderファイルは不要だがfbxファイルのマテリアルを再設定するため）
    * [Hierarchy]に上記のオブジェクト（ufoとmissile）をドラッグ
    * Gameビュー]のサイズを16:9（1920x1080）にする

1. UFOとミサイルのマテリアルを再設定（外れている場合）
    * [Project]-[Assets]-[ufo]-[Inspector]-[Materials]で[blue]、[red]、[white]、[yellow]が "None(Material)" になっている場合、右端の[⦿]を押し、該当のマテリアルを選択し[Apply]ボタンをクリック
    * 同様にmissileもマテリアルを再設定する

1. UFOの位置の調整

    * [ufo]-[Inspector]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |**-14**|**3.5**|**3**|

1. ミサイルの位置･角度の調整

    * [ufo]-[Inspector]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |0|**-1**|**-6.5**|
    
    * [ufo]-[Inspector]-[Transform]-[Rotation]

        |X|Y|Z|
        |:--|:--|:--:|
        |**-25**|0|0|

1. ミサイル発射ボタンを作成
    * uGUIのButtonを配置：[GameObject]-[UI]-[Button]
    * オブジェクト名を変更：[Canvas]-[Button]-[Inspector]の"Button"→"Button001"に変更
    * 位置･幅･高さを変更：[Hierarchy]-[Canvas]-[Button001]-[Inspector]

        |PosX|PosY|PosZ|
        |:--|:--|:--:|
        |**0**|**-460**|0|

        |Width|Height|
        |:--|:--|
        |**400**|**200**| 

    * スケールを変更：[Hierarchy]-[Canvas]-[Button001]-[Inspector]-[Scale]

        |X|Y|Z|
        |:--|:--|:--:|
        |**0.5**|**0.5**|0|

    * 表示文字の変更：[Hierarchy]-[Canvas]-[StartStopButton]-[Text]-[Inspector]-[Text]-[Text]を"Button"→"GO"に変更

    * 表示文字のサイズを変更：[Hierarchy]-[Canvas]-[StartStopButton]-[Text]-[Inspector]-[Text]-[Charactor]-[FontSize]を14→100

1. パーティクル（爆発）のダウンロード＆設置
    * [AssetSore]タブを選択し「**Unity Particle Pack**」を検索し選択
    * [インポート]ボタンをクリック
    * 途中、次の項目のみ選択し[Import]  
        * [EffectExamples]-[Fire&ExplosionEffects]-[Prefabs]-[BigExplosion.prefab]
        * [EffectExamples]-[Fire&ExplosionEffects]-[Materials]の全項目
        * [EffectExamples]-[Fire&ExplosionEffects]-[Textures]の全項目
    * [Project]-[Assets]-[EffectExamples]-[Fire&ExplosionEffects]-[Prefabs]-[BigExplosion]を[Hierarchy]のルートにドラッグ  
    ※ufo上にドラッグするとネスト化されます

1. パーティクルの詳細設定
    * 位置の変更：[Hierarchy]-[BigExplosion]-[Inspector]-[Transform]

        |PosX|PosY|PosZ|
        |:--|:--|:--:|
        |**0**|**0**|**0**|
    
    * 初期値の変更：[Hierarchy]-[BigExplosion]-[Inspector]-[ParicleSystem]
        * Looping：OFF
        * Play On Awake：OFF

1. 物理演算コンポーネント（**Rigidbody**）の設置
    * UFOに設置  
    [Hierarchy]-[ufo]-[Inspector]-[AddComponent]-[Physics]-[Rigidbody]
    * ミサイルに設置  
    [Hierarchy]-[missile]-[Inspector]-[AddComponent]-[Physics]-[Rigidbody]

1. コライダ（衝突判定領域）の設置
    * UFOに設置  
    [Hierarchy]-[ufo]-[Inspector]-[AddComponent]-[Physics]-[SphereCollider]（球型）  
    ※[Inspector]-[SphereCollider]-[EditCollider]で大きさを調整（任意）
    * ミサイルに設置  
    [Hierarchy]-[missile]]-[Inspector]-[AddComponent]-[Physics]-[CapsuleCollider]（カプセル型）

1. メインスクリプト（Main.cs）の用意
    * [Object]-[CreateEmpty]で空のGameObjectを作成（名前は"God"など任意）
    * [Assets]-[Create]-[C# Script]で名前は"Main"とする
    * 上記の空のGameObject（"God"）の[Inspector]に、上記のC#（Main.cs）をドラッグ（アタッチ）

1. UFO用スクリプト（Ufo.cs）の用意
    * [Assets]-[Create]-[C# Script]で名前は"Ufo"とする
    * [Hierarchy]-[ufo]-[Inspector]に、上記のC#（Ufo.cs）をドラッグ（アタッチ）

1. ボタン用スクリプト（MissileButton.cs）の用意
    * [Assets]-[Create]-[C# Script]で名前は"MissileButton"とする
    * [Hierarchy]-[Canvas]-[Button001]-[Inspector]-[Button(Script)]の直下に、上記のC#（MissileButton.cs）をドラッグ（アタッチ）

1. Main.csの記述（変更）
    ```
    //Main.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    using System; //Mathに必要

    public class Main : MonoBehaviour {
        private GameObject _ufo;
        private GameObject _missile;
        private GameObject _button;
        private Vector3 _originMissilePos;
        private Vector3 _originUfoPos;
        private Quaternion _originUfoQuater;
        private Quaternion _originMissileQuater;

        void Start () {
            _ufo = GameObject.Find("ufo");
            _missile = GameObject.Find("missile");
            _button = GameObject.Find("Button001");

            //デフォルトの位置の保存
            _originMissilePos = _missile.transform.position;
            _originUfoPos = _ufo.transform.position;

            //デフォルトの角度の保存
            _originUfoQuater = _ufo.transform.rotation;
            _originMissileQuater = _missile.transform.rotation;

            //初期化
            InitUFO();
            InitMissile();

            //ミサイルを落下させないようにする
            _missile.GetComponent<Rigidbody>().useGravity = false;
        }

        void Update () {
            //回転
            _ufo.transform.Rotate(new Vector3(0,0,-10));
            _missile.transform.Rotate(new Vector3(0,0,-10));

            //左→右へ移動（繰返し）
            if (_ufo.transform.position.x < 14) { //UFOが右端へ消えたら
                Vector3 _ufoPos = _ufo.transform.position;
                _ufoPos.x += 0.1f;
                _ufo.transform.position = _ufoPos;
            } else {
                InitUFO(); //初期化
            }

            if (_ufo.transform.position.y < -25) {
                InitUFO(); //初期化
            }

            if (_missile.transform.position.y < -25) {
                InitMissile(); //初期化
            }
        }

        private void InitUFO() {
            //物理処理を削除
            Rigidbody _ufoRigidbody = _ufo.GetComponent<Rigidbody>();
            _ufoRigidbody.useGravity = false;

            //動いてる物体を完全に止める
            _ufoRigidbody.velocity = Vector3.zero;
            _ufoRigidbody.angularVelocity = Vector3.zero;

            //角度を元に戻す
            _ufo.transform.rotation = _originUfoQuater;

            //画面の左端に移動
            _ufo.transform.position = _originUfoPos;
        }

        private void InitMissile() {
            //物理処理を削除
            Rigidbody _missileRigidbody = _missile.GetComponent<Rigidbody>();
            _missileRigidbody.useGravity = false;

            //画面の手前に移動
            _missile.transform.position = _originMissilePos;

            //角度を元に戻す
            _missile.transform.rotation = _originMissileQuater;

            //動いてる物体を完全に止める
            _missileRigidbody.velocity = Vector3.zero;
            _missileRigidbody.angularVelocity = Vector3.zero;

            //他のオブジェクトのメソッドを実行（ボタンの有効化）
            _button.GetComponent<MissileButton>().Show();
        }

        public void Shoot() {
            //ミサイルの物理エンジンを有効にする
            _missile.GetComponent<Rigidbody>().useGravity = true;

            //ミサイル発射（Vector3(右,上,前)）
            _missile.GetComponent<Rigidbody>().velocity = new Vector3(0,10,10);

            //ミサイルに力を加える（ミサイル発射の代替）
            //_missile.GetComponent<Rigidbody>().AddForce(0,500,500);
        }
    }
    ```

1. Ufo.csの記述（変更）
    ```
    //Ufo.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class Ufo : MonoBehaviour {
        private GameObject _bigExplosion;
        private ParticleSystem _particle;

        void Start () {
            GetComponent<Rigidbody>().useGravity = false;
            _bigExplosion = GameObject.Find("BigExplosion");
            _particle =_bigExplosion.GetComponent<ParticleSystem>();
            _particle.Stop();
        }

        void OnCollisionEnter(Collision arg) { //衝突判定
            GetComponent<Rigidbody>().useGravity = true; //落下

            //パーティクル再生（爆発）
            Vector3 _thisPos = _bigExplosion.transform.position;
            _thisPos.x = arg.transform.position.x;
            _thisPos.y = arg.transform.position.y;
            _bigExplosion.transform.position = _thisPos;
            _particle.Play();

            //爆発の繰返しを止める
            Invoke("BigExplosionDepth", _particle.main.duration);
        }
        
        void BigExplosionDepth() {
            _particle.Stop();
            _bigExplosion.SetActive(false);
        }

        public bool IsExplosionActive {
            get { return _bigExplosion.active; } //thisは省略
            set { _bigExplosion.SetActive(value); } //valueは決め打ち
        }
    }
    ```

1. MissileButton.csの記述（変更）
    ```
    //MissileButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;
    using UnityEngine.UI;

    public class MissileButton : MonoBehaviour {
        private GameObject _god;
        private GameObject _ufo;

        void Start () {
            _god = GameObject.Find("God");
            _ufo = GameObject.Find("ufo");
        }

        public void OnClick() {
            _god.SendMessage("Shoot");
            
            //他のオブジェクトのメソッドを実行（ボタンの無効化）
            GetComponent<MissileButton>().Hide();

            //爆発の有効化
            _ufo.GetComponent<Ufo>().IsExplosionActive = true;
        }

        public void Show() { //カスタムメソッド（外部からアクセス）
            this.GetComponent<Button>().interactable = true;
        }

        public void Hide() { //カスタムメソッド（外部からアクセス）
            this.GetComponent<Button>().interactable = false;
        }
    }
    ```

    * OnClick()メソッドの有効化：  
    [Hierarchy]-[Canvas]-[Button001]-[Inspector]-[Button(Script)]-[OnClick()]の[+]を選択し、[None（Object）]→[Scene]-[Button001]に変更し、[NoFunction]→[MissileButton]-[OnClick]を選択（MissileButton.OnClickになる）  
    （__非常にわかりにくい操作__）

1. [再生]ボタンを押すか、[出力](#出力)して確認

※完成したAndroid用インストーラ（apkファイル）は[こちら](https://mubirou.github.io/Unity3D/introduction/apk/014.apk)

※完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/014.zip)

実行環境：Unity 2018.2 Personal、Ubuntu 18.0.4 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年11月05日  


<a name="015"></a>
# <b>015 Timeline Anime</b>

<a name="015_1"></a>

## Animation版

1. 空のGameObjectを作成
    * [Hierarchy]-[Create]-[CreateEmpty]
    * 名前を"GameObject"→"CubeAll"に変更（任意）
 
1. Cube①を作成
    * [Hierarchy]-[Create]-[3DObject]-[Cube]
    * 名前を"GameObject"→"Cube1"に変更
    * [Hierarchy]上で上記の"CubeAll"の入れ子にする
    * 位置の変更：[Hierarchy]-[CubeAll]-[Cube1]-[Inspector]-[Transform]-[Position]

    |X|Y|Z|
    |:--|:--|:--:|
    |**-3.9**|0|0|

1. Cube②〜⑦を作成
    * 上記を[Copy]＆[Paste]しながら"Cube2"〜"Cube7"を作成
    * 位置（X）を②から順に「**-2.6**」「**-1.3**」「**0**」「**1.3**」「**2.6**」「**3.9**」にする
    * [Project]-[Create]-[Material]から着色するとわかりやすい（任意）

1. 床を作成  
    * [Hierarchy]-[Create]-[3DObject]-[Plane]
    * 位置の変更：[Hierarchy]-[Plne]-[Transform]-[Position]

    |X|Y|Z|
    |:--|:--|:--:|
    |0|**-0.5**|0|

1. Animationの準備
    * [Window]-[Animation]-[Animation]でAnimationウインドウを開く
    * [Hierarchy]-[CubeAll]を選択
    * [Animation]ウインドウ内の[Create]ボタンをクリック（名前は"AnimationCubeAll"）
    * [AddProperty]-[Cube1]-[Transform]-[Position]-[+]を選択  

    ![015_1](https://mubirou.github.io/Unity3D/introduction/jpg/015_1.jpg)

    * 同様にCube②〜⑦も設定  

    ![015_2](https://mubirou.github.io/Unity3D/introduction/jpg/015_2.jpg)

1. Animationの設定
    * [Animation]ウインドウ上部にある録音ボタン[<font color="Red">●</font>]を選択
    * [Animation]ウインドウ下部にある[Curves]ボタンを選択
    * [Animation]-[Cube1:Position]-[Position.y]を選択
    * カーブ上のポイントを選択し[右クリック]-[Broken]に変更して適当に調整

    ![015_3](https://mubirou.github.io/Unity3D/introduction/jpg/015_3.jpg)

    * [Animation]ウインドウの再生ボタン[▶]で確認しながら調整を繰返す
    * 同様にCube②〜⑦も設定
    * タイミングをずらすなどして演出  

    ![015_4](https://mubirou.github.io/Unity3D/introduction/jpg/015_4.jpg)

## Timeline版

1. [Animation版](#015_1)と同じくCube①〜⑦と床を作成

1. Timelineの準備
    * [Window]-[Cequencing]-[Timeline]でTimelineウインドウを開く
    * [Hierarchy]-[CubeAll]を選択
    * [Timeline]ウインドウ内の[Create]ボタンをクリック（名前は"CubeAllTimeline"のまま）
    * [Hierarychy]-[CubeAll]-[Cube1]を[Timeline]上にドラッグ＆ドロップ  

    ![015_5](https://mubirou.github.io/Unity3D/introduction/jpg/015_5.jpg)

    * 最初からあった[CubeAll(Animator)]は今回は削除

1. Timelineの設定
    * [Timeline]ウインドウ上の[Cube1]の録音ボタン[<font color="Red">●</font>]を押して適当に調整（カーブボタンを使って微調整）  

    ![015_6](https://mubirou.github.io/Unity3D/introduction/jpg/015_6.jpg)

    * 同様にCube②〜⑦も設定（カーブ以外は同時に調整可能）
    * [Cube1]のシーケンス上で[右クリック]-[**ConvertToClipTrack]で「アニメーションクリップ」に変換（Cube②〜⑦も同様）  

    ![015_7](https://mubirou.github.io/Unity3D/introduction/jpg/015_7.jpg)

    * タイミングをずらすなどして演出（シーケンスのコピーも可）  

    ![015_8](https://mubirou.github.io/Unity3D/introduction/jpg/015_8.jpg)

    * ループさせる場合は[Hierarchy]-[CubeAll]-[Inspector]-[PlayableDirector]-[WrapMode]を[Loop]にする


※完成したプロジェクトは[こちら](https://mubirou.github.io/Unity3D/introduction/project/015_1.zip)（Animation版）
と[こちら](https://mubirou.github.io/Unity3D/introduction/project/015_2.zip)（Timeline版）

実行環境：Unity 2018.2 Personal、Ubuntu 18.0.4 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年11月26日  


<a name="016"></a>
# <b>016 Puppet Control</b>

1. アクション付きロボットの作成  
    * [『ブレンダーからはじめよう!／原田大輔著』](https://amzn.to/2vzog2t)を参考に、アクション（①Stop ②Walk ③Run）付きの[ロボット（.blend）](https://mubirou.github.io/Blender/introduction/blend/013_011.blend)を作成
    * Unityで読込んだ際に不要な、地面（平面）･Lamp･Camera･Worldを削除
    * [ファイル]-[エクスポート]-[**FBX（.fbx）**]で出力（
    [robot.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/robot.fbx)）

1. Unityにロボットを読込む
    * プロジェクトの[Assets]フォルダに上記のfbxファイルを保存
    * [Hierarchy]に上記のオブジェクト（robot）をドラッグ
    * [Gameビュー]のサイズを16:9（1920x1080）にする

1. 床を作成  
    * [Hierarchy]-[Create]-[3DObject]-[Plane]
    * 位置の変更：[Hierarchy]-[Plne]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |**0**|**0**|**0**|

    * サイズの変更：[Hierarchy]-[Plne]-[Transform]-[Scale]

        |X|Y|Z|
        |:--|:--|:--:|
        |**10**|**10**|**10**|

1. ロボットの位置･角度の調整
    * [Hierarchy]-[robot]-[Inspector]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |**0**|**0**|**0**|
    
    * [Hierarchy]-[robot]-[Inspector]-[Transform]-[Rotation]

        |X|Y|Z|
        |:--|:--|:--:|
        |0|**-180**|0|

1. カメラの位置の調整
    * [Hierarchy]-[MainCamera]-[Inspector]-[Transform]-[Position]

        |X|Y|Z|
        |:--|:--|:--:|
        |0|**2.75**|-10|

1. ロボットを動かしてみる
    * [Project]-[Create]-[**Animator Controller**]を選択（名前は"robotController"にする）
    * [Hierarchy]-[robot]-[Inspector]-[Animator]-[**Controller**]-[⦿]で上記で作成した"robotController"を選択
    * [Project]-[Assets]-[robotController]-[Inspector]-[Open]を選択（**Animatorウィンドウ**が開く）
    * [Project]-[Assets]-[robot]-[▶]の中から、①Armature|Stop ②Armature|Run ③Armature|Run を上記の[Animatorウィンドウ]にドラッグ＆ドロップ
    * [Animatorウィンドウ]-[Armature|Stop]上で右クリック→[Maketransition]→そのまま[Armature|Walk]へドラッグ＆ドロップ  
    ※[→]を選択後[Delete]ボタンで削除可能
    * 下図のように①Armature|Stop ②Armature|Run ③Armature|Run を双方向で連結させる

    ![016_1](https://mubirou.github.io/Unity3D/introduction/jpg/016_1.jpg)

    * [Hierarchy]-[robot]を選択した状態で再生ボタン[▶]で動作確認  
    ※①Stop ②Walk ③Run が連続して実行されるはずです

1. STOPボタンの作成
    * uGUIのButtonを配置：[GameObject]-[UI]-[**Button**]
    * オブジェクト名を変更：[Inspector]の"Button"→"Button_Stop"に変更
    * 表示文字の変更：[Hierarchy]-[Canvas]-[Button_Stop]-[Text]-[Inspector]-[Text]-[Text]を"Button"→"STOP"に変更
    * 位置･サイズの変更：[Hierarchy]-[Canvas]-[Button_Stop]-[Inspector]-[RectTransform]

        |PosX|PosY|PosZ|
        |:--|:--|:--|
        |**-735**|**-442**|0|

        |Width|Height|
        |:--|:--|
        |**640**|**180**|

    * スケールの変更：[Hierarchy]-[Canvas]-[Button_Stop]-[Inspector]-[RectTransform]-[Scale]

        |X|Y|Z|
        |:--|:--|:--|
        |**0.5**|**0.5**|1|

    * フォントサイズの変更：[Hierarchy]-[Canvas]-[Button_Stop]-[Text]-[Inspector]-[Text]-[Character]

        |Property|Value|
        |:--|:--|
        |FontStyle|**Bold**|
        |FontSize|**100**|

1. WALK･RUNボタンの作成
    * STOPボタンを[Copy]-[Paste]でWALK･RUNも作成
    * 名前は"Button_Walk"･"Button_Run"にする
    * "Button_Walk"の位置を変更

        |PosX|PosY|PosZ|
        |:--|:--|:--|
        |**-387**|-442|0|

    * "Button_Run"の位置を変更

        |PosX|PosY|PosZ|
        |:--|:--|:--|
        |**-43**|-442|0|

1. Animator Controllerにパラメータを設定
    * [Project]-[Assets]-[robotController]-[Open]を選択（**Animatorウィンドウ**が開く）
    * [Animator]-[**Parameters**]タブを選択
    * [+]→[Bool]で "**isWalk**" パラメータを作成（初期値：✔なし = false）
    * [+]→[Bool]で "**isRun**" パラメータを作成（初期：✔なし）

1. 遷移（①Stop↔②Walk↔③Run等）の条件を設定
    1. ①Stop→②Walk
        * ①Stop ②Walk 間の [→] を選択し [Inspector]-[**Conditions**]-[+] を選択（以下同様）
        * [**isWalk**]：**true**
        * [**isRun**]：false  
        ![016_2](https://mubirou.github.io/Unity3D/introduction/jpg/016_2.jpg)
    
    1. ②Walk→③Run
        * [**isWalk**]：false
        * [**isRun**]：**true**

    1. ③Run→①Stop
        * [**isWalk**]：false
        * [**isRun**]：false
    
    1. ①Stop→③Run
        * [**isWalk**]：false
        * [**isRun**]：**true**
    
    1. ③Run→②Walk
        * [**isWalk**]：**true**
        * [**isRun**]：false

    1. ②Walk→①Stop
        * [**isWalk**]：false
        * [**isRun**]：false

1. STOPボタン用スクリプト（**StopButton.cs**）の用意
    * [Assets]-[Create]-[C# Script]で名前は"StopButton"とする
    * [Hierarchy]-[Canvas]-[Button_Stop]-[Inspector]-[Button(Script)]の直下に、上記のC#（**StopButton.cs**）をドラッグ（アタッチ）

1. WALK･RUNボタン用スクリプト（**WalkButton.cs** / **RunButton.cs**）の用意
    * [Assets]-[Create]-[C# Script]で名前は"WalkButton"（**WalkButton.cs**）とする
    * [Assets]-[Create]-[C# Script]で名前は"RunButton"（**RunButton.cs**）とする
    * STOPボタン同様に、[Button_Walk]にC#（**WalkButton.cs**）を、[Button_Run]にC#（**RunButton.cs**）をアタッチ

1. スクリプト（**StopButton.cs**）の記述
    ```
    //StopButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class StopButton : MonoBehaviour {
        private GameObject _robot;
        private Animator _robotAnim;

        void Start () {
            _robot = GameObject.Find("robot");
            _robotAnim = _robot.GetComponent<Animator>();
        }
        
        public void OnClick() {
            _robotAnim.SetBool("isWalk", false);
            _robotAnim.SetBool("isRun", false);
        }
    }
    ```

1. スクリプト（**WalkButton.cs**）の記述
    ```
    //WalkButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class WalkButton : MonoBehaviour {
        private GameObject _robot;
        private Animator _robotAnim;

        void Start () {
            _robot = GameObject.Find("robot");
            _robotAnim = _robot.GetComponent<Animator>();
        }
        
        public void OnClick() {
            _robotAnim.SetBool("isWalk", true);
            _robotAnim.SetBool("isRun", false);
        }
    }
    ```

1. スクリプト（**RunButton.cs**）の記述
    ```
    //RunButton.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class RunButton : MonoBehaviour {
        private GameObject _robot;
        private Animator _robotAnim;

        void Start () {
            _robot = GameObject.Find("robot");
            _robotAnim = _robot.GetComponent<Animator>();
        }
        
        public void OnClick() {
            _robotAnim.SetBool("isWalk", false);
            _robotAnim.SetBool("isRun", true);
        }
    }
    ```

1. OnClick()メソッドの有効化（STOPボタン用）
    * [Hierarchy]-[Canvas]-[Button_Stop]-[Inspector]-[Button]-[OnClick()]-[+]を選択
    * [None（Object）]-[⦿]→[**Sceneタブ**]-[Button_Stop]をダブルクリック
    * [NoFunction]→[StopButton]-[OnClick]を選択（**StopButton.OnClick**と表示される）  
    ![016_3](https://mubirou.github.io/Unity3D/introduction/jpg/016_3.jpg)

1. OnClick()メソッドの有効化（WALKボタン用）
    * [Hierarchy]-[Canvas]-[Button_Walk]-[Inspector]-[Button]-[OnClick()]-[+]を選択
    * [None（Object）]-[⦿]→[**Sceneタブ**]-[Button_Walk]をダブルクリック
    * [NoFunction]→[WalkButton]-[OnClick]を選択（**WalkButton.OnClick**と表示される）

1. OnClick()メソッドの有効化（RUNボタン用）
    * [Hierarchy]-[Canvas]-[Button_Run]-[Inspector]-[Button]-[OnClick()]-[+]を選択
    * [None（Object）]-[⦿]→[**Sceneタブ**]-[Button_Run]をダブルクリック
    * [NoFunction]→[RunButton]-[OnClick]を選択（**RunButton.OnClick**と表示される）

1. 再生テスト
    * [Hierarchy]-[robot]を選択した状態で再生ボタン[▶]で動作確認
    * ①Stop ②Walk ③Run を選択
    * ②Walk ③Run の動きがループしません

1. アニメーションをループさせる
    * [Project]-[Assets]-[robot]-[▶]-[Armature|**Walk**]-[Edit...]を選択
    * [Inspector]-[Animation]-[**Loop Time**]を✔
    * 同様に[Armature|**Run**]の[Loop Time]も✔

1. [再生]ボタンを押すか、[出力](#出力)して確認

※完成インストールファイル（Android用.apkファイル）は[こちら](https://mubirou.github.io/Unity3D/introduction/apk/016.apk)

※完成プロジェクトを[ダウンロード](https://mubirou.github.io/Unity3D/introduction/project/016.zip)

実行環境：Unity 2018.2 Personal、Ubuntu 18.0.4 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2018年12月08日


<a name="017"></a>
# <b>017 Humanoid</b>

#### ◆FBXファイルの読み込み

1. [Blenderで作成](https://github.com/mubirou/Blender/tree/master/introduction#016_003)した人間型の[.fbx](https://mubirou.github.io/Unity3D/introduction/fbx/human.fbx)ファイルをUnityの[Assets]フォルダにコピーする

#### ◆人間型オブジェクトのHumanoid化

1. [Project]-[Assets]に現れた[human.fbx]を[Hierarchy]にドラッグ＆ドロップ
1. [Project]-[Assets]-[human]を選択
1. [Inspector]-[Rig]-[AnimationType]を[Generic]→[Humanoid]に変更
1. [Apply]（適用）を選択→[Configure...]を選択  
    ![017_1](https://mubirou.github.io/Unity3D/introduction/jpg/017_1.jpg)  
    ※Blenderと名前が一致していれば上図の通りになります  
    ※今回は[Head][LeftHand][RightHand]は省略
1. [Muscles&Settings]を選択し各スライダーバーを動かしてポージングできれば成功  
    ![017_2](https://mubirou.github.io/Unity3D/introduction/jpg/017_2.jpg)  

※参考プロジェクトは[こちら](https://mubirou.github.io/Unity3D/introduction/project/017.zip)

実行環境：Unity 2018.2 Personal、Ubuntu 18.0.4 LTS、Blender 2.79、Android 8.0  
作成者：夢寐郎  
作成日：2019年01月22日


<a name="018"></a>
# <b>018 AR入門</b>

事前に Android の場合の[出力](https://github.com/mubirou/Unity/tree/master/introduction#%E5%87%BA%E5%8A%9B)設定をしておきます

1. ARCore SDK for Unity のダウンロード  
    1. https://github.com/google-ar/arcore-unity-sdk/releases にアクセス
    1. 最新版の [arcore-unity-sdk-vX.X.X.unitypackage] をダウンロード

1. Unity を起動し、Project を保存
1. [Assets]-[ImportPackage]-[CustomPackage...] から上記の [.unitypackage] ファイルをインポート
1. [Project]-[Assets]-[GoogleARCore]-[Examples]-[ComputerVision]-[Scenes]-[ComputerVision] を開く
1. [File]-[BuildSettings...]-[AddOpenScenes] ボタンを押して [GoogleARCore/Examples/ComputerVision/Scenes/ComputerVision] をビルドの対象とする
1. [PlaySEttings...] を選択し各種設定
    * Other Settings  
        * Multithreaded Rendering : ✔を外す
        * Package Name : com.mubirou.app001 等
        * Minimum API Level : Andoid 7.0 "Nougat"(API Leve... 等
    * XR Settings  
        * ARCore Supported : ✔
1. [File]-[BuildSettings...]-[Build] ボタンを押して出力
1. Android 端末とPCを接続して、上記で作成した [.apk] ファイルをインストール
1. インストール途中、[ARCorebyGoogle] のダウンロードが要求されたら支持に従う

（注意）  
[ARCore対応端末一覧](https://qiita.com/namiwavess/items/088605ffdd9062d57bd8)に無い端末の場合、[ARCorebyGoogle] のイントール途中、「お使いのデバイスはこのバージョンに対応していません。」と表示されます（HUAWEI Mate9 は対象外）


実行環境：Unity 2018.3 Personal、Ubuntu 18.0.4 LTS、Android 9.0  
作成者：夢寐郎  
作成日：2019年05月29日


<a name="019"></a>
# <b>019 SQLite操作</b>

この項目は書きかけの項目です。

1. **SQLiteUnityKit** のダウンロード  
    1. https://github.com/Busta117/SQLiteUnityKit にアクセス
    1. [Clone of download] ボタン→ [Download ZIP] を選択
    1. ダウンロードした [SQLiteUnityKit-master.zip] ファイルを展開
    1. 展開した [SQLiteUnityKit-master] フォルダ内の [libsqlite3.so] を次の場所に移動（フォルダは自作）  
        ```
        （プロジェクト名）/Assets/Plugin/Android/libsqlite3.so
        ```
    1. 同じく [SQLiteUnityKit-master] フォルダ内の [DataTable.cs] と [SqliteDatabase.cs] を次の場所に移動  
        ```
         （プロジェクタ名）/Assets/Script/SQLite/
        ```

1. 端末でデータベースを作成  
    ```
    $ cd /home/（ユーザ名）/デスクトップ/（プロジェクト名）/Assets/StreamingAssets
    $ sqlite3 sample.db
    sqlite> CREATE TABLE IF NOT EXISTS ranking_tb(name TEXT, point INTEGER); ←ここでファイルが生成
    sqlite> INSERT INTO ranking_tb VALUES('MUBIROU', 1234);
    sqlite> .exit
    ```

1. Unityのプロジェクタを作成  
    （今回は /home/（ユーザ名）/デスクトップ/UnitySQLite とする）
1. 以下のスクリプトを作成して実行  
    ```
    //Assets/Script/Main.cs
    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class Main : MonoBehaviour {
        void Start() {
            SqliteDatabase _db = new SqliteDatabase("sample.db");

            string _sql = "SELECT * FROM ranking_tb";
            DataTable _data = _db.ExecuteQuery(_sql);

            foreach (DataRow _tmp in  _data.Rows) {
                Debug.Log(_tmp["name"]);
                Debug.Log(_tmp["point"]);
            }
        }
    }
    ```

実行環境：Unity 2019.1 Personal、Ubuntu 18.0.4 LTS、Android 9.0  
作成者：夢寐郎  
作成日：2019年0X月XX日


© 2018-2019 夢寐郎