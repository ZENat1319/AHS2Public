# 自己責任

# AutoHealthSurvey2Public
Formsを勝手に提出してくれるやつ(一部環境限定版)  
Original Repo->https://github.com/siketyan/AutoHealthSurvey  
Original Author->https://github.com/siketyan

## 使い方
1. このリポジトリをForkボタン(PCでは右上)からForkする スマホは知らん
2. Node.jsのワークフローを有効化する  
   https://docs.github.com/ja/actions/managing-workflow-runs/disabling-and-enabling-a-workflow#disabling-a-workflow
3. `config.yaml` は編集しなくてよろしい
4. `.github/workflows/node.yml` の6行目で提出時間を決める
5. このリポジトリのSettingsのSecretsでNew repository secretをクリックして以下の変数を作成
   Name : `MICROSOFT_EMAIL`   , Value : **Office365のメアド**  
   Name : `MICROSOFT_PASSWORD`, Value : **Office365のパスワード**  
   Name : `FORMS_URL`         , Value : **FormsのURL**
6. 以上

## Troubleshooting
If the timeout error occurs at clearing Local Storage, try to use virtual or real X display with headful mode.
```console
$ CHROMIUM_HEADFUL=1 npm start
```
