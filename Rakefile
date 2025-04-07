desc "Given a title as an argument, create a new post file"
task :write, [:title, :titletwo, :titlethree, :category] do |t, args|
  filename = "#{Time.now.strftime('%Y-%m-%d')}-#{args.title.gsub(/\s/, '_').downcase}.md"
  path = File.join("_posts", filename)
  if File.exist? path; raise RuntimeError.new("Won't clobber #{path}"); end
  File.open(path, 'w') do |file|
    file.write <<-EOS
---
layout: post
title: #{args.title}
title2: #{args.titletwo}
title3: #{args.titlethree}
category: #{args.category}
---
EOS
    end
    puts "Now open #{path} in an editor."
    system ("#{ENV['EDITOR']} #{path}")
end
