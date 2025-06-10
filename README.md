docker run -d \
  --name atlantis \
  -p 4141:4141 \
  -v $(pwd)/repos.yaml:/etc/atlantis/repos.yaml \
  -e ATLANTIS_REPO_CONFIG=/etc/atlantis/repos.yaml \
  -e ATLANTIS_GH_USER=marwenbhriz \
  -e ATLANTIS_GH_TOKEN=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 \
  -e ATLANTIS_GH_WEBHOOK_SECRET=marwen \
  runatlantis/atlantis

  -e ATLANTIS_REPO_WHITELIST=github.com/your-org/* \


docker pull ngrok/ngrok


//ngrok token
1W8x4vCj3sk4XiQ8Rv2wvHowHXq_2tF5Z2vgS9agkCcUgDxqd

docker run -it -e NGROK_AUTHTOKEN=1W8x4vCj3sk4XiQ8Rv2wvHowHXq_2tF5Z2vgS9agkCcUgDxqd ngrok/ngrok http 4141

Forwarding                    https://0bbf-175-129-140-78.ngrok-free.app -> http://localhost:4141    


new test


curl -X POST \
  -H "Content-Type: application/json" \
  -H "X-GitHub-Event: pull_request" \
  -d '{"action": "opened", "pull_request": {"number": 1}}' \
  https://da9c-240f-84-e791-1-4837-e9af-d549-fb42.ngrok-free.app



  curl -X POST \
  -H "Content-Type: application/json" \
  -H "X-GitHub-Event: pull_request" \
  -d '{
    "action": "opened",
    "number": 1,
    "pull_request": {
      "number": 1,
      "head": {
        "sha": "abc123",
        "ref": "test-branch",
        "repo": {
          "full_name": "marwenbhriz/atlantis",
          "clone_url": "https://github.com/marwenbhriz/atlantis.git"
        }
      },
      "base": {
        "ref": "main",
        "repo": {
          "full_name": "marwenbhriz/atlantis",
          "clone_url": "https://github.com/marwenbhriz/atlantis.git"
        }
      }
    },
    "repository": {
      "full_name": "marwenbhriz/atlantis",
      "clone_url": "https://github.com/marwenbhriz/atlantis.git"
    }
  }' \
  https://da9c-240f-84-e791-1-4837-e9af-d549-fb42.ngrok-free.app/events



sss