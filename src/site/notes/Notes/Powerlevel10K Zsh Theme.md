---
{"dg-publish":true,"permalink":"/notes/powerlevel10-k-zsh-theme/"}
---




# Powerlevel10K Zsh Theme
- [romkatv/powerlevel10k: A Zsh theme (github.com)](https://github.com/romkatv/powerlevel10k)
- [[Notes/File .p10k.zsh\|File .p10k.zsh]]

### How to install?
1. [[Notes/How to install Oh My Zsh\|Install Zsh & Oh-My-Zsh]]
2. Install p10k theme:
	1. `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
	2. Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.
3. Copy [[Notes/File .p10k.zsh\|File .p10k.zsh]] (replace existing)