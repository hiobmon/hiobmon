task :default do
  puts "Running CI tasks..."

  # Travis CI will grab _site/* from develop branch and push it to master branch
  sh("JEKYLL_ENV=production bundle exec jekyll build")
  puts "Jekyll successfully built"
end
