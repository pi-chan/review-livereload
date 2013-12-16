guard 'shell' do

  watch(/README.md$/) do |m|
    `./bin/md2review #{m[0]} > review/README.re`
    Dir.chdir("./review") do
      `../bin/review-compile --target=html README.re > ../html/index.html`
    end
  end
  
  watch(/.*markdown\/(.*)\.md$/) do |m|
    `./bin/md2review #{m[0]} > review/#{m[1]}.re`
    Dir.chdir("./review") do
      `../bin/review-compile --target=html #{m[1]}.re > ../html/#{m[1]}.html`
    end
    puts "built #{m[1]}.html"
  end
end

guard 'livereload', :apply_js_live => false do
  watch(%r{html/.+\.(html)})
end

