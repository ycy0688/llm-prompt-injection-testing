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

**主選單導覽**：以選單方式提供多種測試選項，包括：
\- View Attack Examples：列出常見攻擊 prompt。
\- Interactive Testing：手動輸入 prompt 進行測試。
\- Integrate with Existing Framework： 與外部程式`main.py`結合。
\- Exit。
  
## 整合於本專案的主選單腳本中的2跟3，也可以獨立執行測試：
`demo_prompt_injection.py`用於互動測試模型是否能正確識別並拒絕提示注入攻擊。

執行：
```bash
python demo_prompt_injection.py
```

 `main.py` 檔案來源於開源專案 [llm-security](https://github.com/greshake/llm-security/tree/main)，此專案中提供了各種攻擊媒介和技術的示範。

```bash
python main.py
```

**關於 main.py 的詳細功能與用法，請參考原作者的完整說明文件：**
- 🔗 [GitHub Repository](https://github.com/greshake/llm-security)

---
本檔案設計簡單易用，適合各種 LLM 安全測試場景，後續可依需求擴充或整合其他測試腳本。
