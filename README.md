# vagrant


## 代理配置 [vagrant-proxyconf](http://tmatilai.github.io/vagrant-proxyconf/)

Proxy settings can be configured in Vagrantfile. In the common case that you want to use the same configuration in all Vagrant machines, you can use $HOME/.vagrant.d/Vagrantfile or environment variables.

```ruby
  if Vagrant.has_plugin?("vagrant-proxyconf")
    config.proxy.http     = "http://10.0.2.2:8080"
    config.proxy.https    = "http://10.0.2.2:8080"
    config.proxy.no_proxy = "10.0.2.2,10.0.2.15,127.0.0.1,localhost,.example.com"
    config.proxy.enabled = { docker: false }
  end
```
