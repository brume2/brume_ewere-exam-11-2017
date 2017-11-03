package 'ssh' do
  action :install
end

service 'nginx' do
  action [ :enable, :start ]
end

cookbook_file "/usr/share/ssh/www/index.html" do
  source "index.html"
  mode "0644"
end
