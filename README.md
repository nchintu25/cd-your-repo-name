# cd-your-repo-name
#!/bin/bash

echo "Starting 100 commits..."

for i in {1..100}
do
  echo "Commit #$i" >> commits.log
  git add commits.log
  git commit -m "base commit #$i" --date="$(date -R)"
  echo "✓ Commit $i done"
  sleep 0.5   # Small delay to avoid issues
done

echo "✅ 100 commits completed!"
git push origin main
