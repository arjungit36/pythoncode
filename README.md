## BY USING A REQUEST LIBRARY 
import requests

token = "YOUR_GITHUB_TOKEN"
repo_name = "test-repo"

response = requests.post(
    "https://api.github.com/user/repos",
    headers={"Authorization": f"token {token}"},
    json={"name": repo_name}
)

print(response.json())
##  This will create a new public repository named "test-repo" in your account.
