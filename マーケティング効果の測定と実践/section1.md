# マーケティング・マネジメントのための市場反応モデル

## Keywords
    - 売上反応関数 sales response functions
    - 市場シェアモデル market share models
    - 離散選択モデル discrete choice models
    - 市場構造分析 market structure analysis
    - 軽量経済時系列分析 ETS (Econommetric and timeseries analysis)
    - 意思決定ルール decision rule
    - 同時方程式システム (simultaneous-equation system)
    - 逐次モデル (recursive model)

## 市場反応モデル
    - 価格の設定、広告支出の配分、売上高の予測、マーケティング家鋭角の効果検証
    - 分野の大きさ1億2500万ドル

## マーケティングシステムのモデリング
    - ETSではマーケティングミックス変数と業績指標の関係を表すことが目的
    - 一番シンプルに考えた場合売上反応関数は
        Q_t = f(A_t, E_t)
         ... Q_t: sales
             A_t: Ad
             E_t: Environmental factor
    - 意思決定ルールがある場合もある
        A_t = f(P_t, Q_t-1)
         ... P_t-1: Price

    - 行いたいことは A* 最適広告予算 を明らかにすること。

    - 単純化の方法としてモデルを確率的な誤差のある線形関係を仮定することがあり、これにより軽量経済モデルを記述する。(これにより実証データを用いて測定でき、それによりパラメータを推定する)

    例えば、
        Q_t = gamma_12 * A_t
            + beta_11 * Y_t
            + beta_12 * N_t
            + beta_13
            + mu_1t
        A_t = beta_21 * R_t-1
            + mu_2t
        gammma: 内生変数のパラメタ
        beta: 先決変数のパラメタ
        mu: 確率的撹乱
    
    1. この場合 mu_1t と mu_2t が独立であれば逐次モデルとして計算できる。
    2. 広告の意思決定ルールが現在または予想される売上に基づくことを仮定した同時方程式システム (simultaneous-equation system) としても表せる。

    一方で変数の関係が明らかではない場合、時系列分析 (timeseries analysis)によって因果関係の方向やラグの構造を見つける。
