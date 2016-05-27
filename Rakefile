require 'html-proofer'

task :build do
  sh "bundle exec jekyll build"
end

task :test do
  # HTMLProofer.check_directory("./_site").run
  # disable_external = false
  # HTMLProofer.check_directory("./_site", opts).run
  # HTMLProofer.check_directory("./_site", {
  HTMLProofer.check_directories(["./_site"], {
    # :alt_ignore => [/.*/],
    # :disable_external => false,
    :file_ignore => [/.*ipynb_.*html/],
    :url_ignore => [/.*github.com\/qiuwch\/unrealcv/],
    # :empty_alt_ignore => true,
    # :checks_to_ignore => ["ImageCheck"],
  }).run
end

task :s do
  sh "bundle exec jekyll s"
end

task :testsub do
  HTMLProofer.check_directories(["./_unrealcv"], {
    :file_ignore => [/.*ipynb_.*html/],
    :url_ignore => [/.*github.com\/qiuwch\/unrealcv/],
  }).run
end

task :syncsub do
  sh "bundle exec jekyll build -d ./_unrealcv/unrealcv/ --config ./_config_subfolder.yml"
  sh "rsync -rav _unrealcv/unrealcv/ weichaoqiu.com:/home/qiuwch/weichaoqiu.com/unrealcv/"
end
