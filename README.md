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