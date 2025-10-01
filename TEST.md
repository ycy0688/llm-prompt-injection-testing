# Prompt Injection Attack Detection
驗證LLM系統能否正確識別和拒絕惡意的提示注入攻擊

🔍 測試類型 / Test Categories:
   • 輸入模糊測試 / Input Fuzzing
   • 系統指令繞過 / System Instruction Bypassing
   • 數據洩露探測 / Data Leakage Probing
   • 角色利用攻擊 / Role Exploitation

✅ 預期結果 / Expected Results:
 安全的LLM應該拒絕所有惡意請求並給出適當的拒絕回應
 Secure LLMs should reject all malicious requests with appropriate refusal responses

### Install dependencies 
   ```bash
   pip install -r requirements.txt
   ```
### How to run
```bash
python start_testing.py
```
`start_testing.py` 是主選單腳本，提供簡單的入口，
協助使用者快速啟動各種Prompt Injection Attack測試。

## 主要功能
- **環境檢查**：自動檢查必要的 Python 套件與 `.env` 檔案，確保測試環境正確。
- **主選單導覽**：以選單方式提供多種測試選項，包括：
  - View Attack Examples：列出常見攻擊 prompt。
  - Interactive Testing：手動輸入 prompt 進行測試。
  - Integrate with Existing Framework： 與外部程式`main.py`結合。
  - Exit。
- **自動執行測試腳本**：根據選擇自動呼叫對應的測試腳本。

專案中的 `main.py` 檔案沿用自[https://github.com/greshake/llm-security/tree/main]，
已整合於主選單腳本，也可獨立執行測試：
```bash
python main.py
```
詳細 package 用法請參考原作者的 README.md。

---
本檔案設計簡單易用，適合各種 LLM 安全測試場景，後續可依需求擴充或整合其他測試腳本。
