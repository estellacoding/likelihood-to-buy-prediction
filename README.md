# 購買機率預測模型

本專案使用**H2O AutoML**建立一個預測模型，用於評估潛在用戶的**購買可能性**。透過預測結果，可以更有效地執行行銷跟進策略，將資源集中在高潛力客戶身上，以提升行銷整體效益。

# 專案目標
- 預測購買可能性: 利用潛在客戶資料預測其是否可能購買產品。
- 行銷策略優化: 根據預測結果將潛在客戶分級，並制定相應的行銷跟進策略。

# 主要功能
- H2O AutoML 自動建模: 自動化訓練多種機器學習模型，並篩選出最佳模型。
- 資料庫整合: 利用 SQLite 管理潛在客戶與交易資料。
- 購買可能性預測: 預測每位潛在客戶的購買機率。
- 行銷策略分級: 根據預測結果，將用戶分類為Hot、Warm、Cold及Non-Target四個等級。

# 專案結構
```
likelihood-to-buy-prediction/
├── Likelihood_To_Buy_Prediction.ipynb  # 主程式
├── database/
│   ├── leads.csv                       # 潛在客戶資料CSV檔
│   ├── transactions.csv                # 交易記錄資料CSV檔
│   └── leads_transactions.db           # SQLite資料庫
└── model/
    └── best_model_h2o                  # 最佳H2O AutoML模型檔案
```

# 最佳模型
model_id|auc|logloss|aucpr|mean_per_class_error|rmse|mse
-|-|-|-|-|-|-
XGBoost_1_AutoML_1_20250224_55852|0.769309|0.168819|0.203925|0.360477|0.20612|0.0424854