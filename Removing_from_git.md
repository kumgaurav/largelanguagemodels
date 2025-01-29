##Remove API Key from Code
Remove the unwanted lines and commit the change
git commit -am "Removed OpenAI API key from code"

##Remove the Commit from Git History
git filter-branch --force --index-filter \
"git rm --cached --ignore-unmatch gen_ai_training/exercise/week5/llmops_frameworks_llamaindex_pinecone_QA_01.ipynb" \
--prune-empty --tag-name-filter cat -- --all

##Force Push to Remove History
git push origin --force --all
