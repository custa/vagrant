# Registry Mirror

运行：
```
ct -platform=vagrant-virtualbox < cl.conf > config.ign
vagrant up
```


### 几个注意的问题：

* Vagrant Windows 共享目录问题

通过 Vagrant 使用 nfs 方式（vagrant-winnfsd插件）共享目录到虚拟机，然后挂载到 registry 容器 /var/lib/registry，访问共享目录会卡死

* Registry Mirror 只能镜像 central Hub

[It’s currently not possible to mirror another private registry. Only the central Hub can be mirrored.](https://docs.docker.com/registry/recipes/mirror/#gotcha)

* 不支持 push 到 Registry Mirror

[Pushing to a registry configured as a pull-through cache is unsupported.](https://docs.docker.com/registry/configuration/#proxy)

