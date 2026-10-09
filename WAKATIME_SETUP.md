# WakaTime Configuration for Profile README

To enable WakaTime stats in your profile README, you need to:

## 1. Create a WakaTime Account
- Sign up at https://wakatime.com
- Install the WakaTime plugin for your IDE/editor (VS Code, PyCharm, Vim, etc.)

## 2. Get Your API Key
- Go to https://wakatime.com/settings/account
- Copy your "Secret API Key"

## 3. Add as GitHub Secret
1. Go to your repository: https://github.com/mrsehajofficial/mrsehajofficial
2. Settings → Secrets and variables → Actions
3. New repository secret:
   - Name: `WAKATIME_API_KEY`
   - Value: [your WakaTime API key]

## 4. Update the Workflow
The workflow will automatically fetch WakaTime stats when the secret is configured.

## Alternative: Manual WakaTime Badge
If you prefer a simple badge without the full stats card, add this to your README:

```markdown
[![WakaTime](https://wakatime.com/badge/user/your-user-id.svg)](https://wakatime.com/@your-username)
```

Replace `your-user-id` and `your-username` with your WakaTime values.