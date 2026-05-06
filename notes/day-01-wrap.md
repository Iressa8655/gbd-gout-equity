# Day 1 Wrap-up, 6 May 2026

## 今天完成了什麼

- Repo `gbd-gout-equity` 建立並 push 到 GitHub
- Python venv + 所有套件安裝完成
- GBD 2023 痛風 DALYs CSV 和 World Bank GDP CSV 下載並放入 `data/raw/`
- `01-load.ipynb`：兩個資料集載入、檢查 shape、dtypes
- `02-eda.ipynb`：histogram、country ranking（170 個國家）、全球時間趨勢 1990-2023
- `03-model.ipynb`：164 個國家 merge、scatter + log regression（R²=0.386）、residual ranking

## 核心發現

殘差前 10 名（實際 DALY rate 遠超 GDP 預測值）：

| 排名 | 國家 | 實際 | 預測 | 殘差 |
|---|---|---|---|---|
| 1 | Georgia | 77.2 | 20.3 | +56.9 |
| 2 | Canada | 75.0 | 28.5 | +46.5 |
| 3 | New Zealand | 72.9 | 27.3 | +45.6 |
| 4 | Australia | 68.1 | 28.7 | +39.4 |
| 5 | Greenland | 55.7 | 30.0 | +25.7 |
| 6 | Japan | 47.3 | 26.7 | +20.7 |
| 7 | Greece | 41.1 | 24.6 | +16.5 |
| 8 | Chile | 39.9 | 23.5 | +16.3 |
| 9 | Palau | 35.1 | 19.0 | +16.1 |
| 10 | China | 37.0 | 21.0 | +16.0 |

## 三件還不完全清楚的事

1. 為什麼 Georgia 的殘差那麼大（+56.9）？是真的治療不足，還是特殊的飲食或遺傳因素？
2. Log transform GDP 的意義：為什麼要取 log 而不是用原始 GDP？
3. R² = 0.386 算高還是低？這個模型夠好用嗎？

## 明天（Day 2, 7 May）先做什麼

1. 解答上面三件事（查資料或問 Claude Code）
2. 把 scatter 圖和 residual ranking 圖合成一張 Fig 4（兩個 panel）
3. 把全部五張圖的 title、軸標籤、字型大小統一，準備 poster 品質
4. 確認 `02-eda.ipynb` 的 country ranking（Fig 2）是否要換成只顯示 Bottom 10 低收入國家（更符合 under-treatment 的論點）
