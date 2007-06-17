require 'hoe'
require 'spec/rake/spectask'

PKG_NAME = "dbf"
PKG_VERSION = "0.5.3"
PKG_FILE_NAME = "#{PKG_NAME}-#{PKG_VERSION}"

Hoe.new PKG_NAME, PKG_VERSION do |p|
  p.rubyforge_name = PKG_NAME
  p.author = "Keith Morrison"
  p.email = "keithm@infused.org"
  p.summary = "A small fast library for reading dBase, xBase, Clipper and FoxPro database files."
  p.description = p.paragraphs_of("README.txt", 1..3).join("\n\n")
  p.changes = p.paragraphs_of("History.txt", 0..1).join("\n\n")
  p.url = "http://dbf.rubyforge.org"
  p.need_tar = true
  p.need_zip = true
end

task :default => [:spec]

desc "Run specs"
Spec::Rake::SpecTask.new :spec do |t|
  t.spec_files = FileList['spec/**/*spec.rb']
end

desc "Run spec docs"
Spec::Rake::SpecTask.new :specdoc do |t|
  t.spec_opts = ["-f specdoc"]
  t.spec_files = FileList['spec/**/*spec.rb']
end