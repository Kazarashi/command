## Useful Command

SSH Certificate / SSH认证 / SSH認証

- make config
```
    Host [server_name]
    Hostname [server_url or ip_address]
    User [server_login_user_name]
    Port 22 #default
    IdentityFile [private_key_path]
    TCPKeepAlive yes #not impossible
    IdentitiesOnly yes #not impossible
    ProxyCommand nc -X connect -x [proxy_ip][proxy_port] %h %p #if proxy works on your network, for OS X
```

PORT FORWARD / 端口转发 / ポート転送

- 用本机10022端口的监听服务器的22端口
```
ssh -L 10022:localhost:22 [server]
```

- 用本机的13306端口通过服务器1监听服务器2的3306端口
```
ssh -t -L 13306:[server2_ip_address]:3306 [server1]
```

SCP - ssh文件/文件夹传送
```
scp [local_path][file_name] [user]@[server]:[server_path]
scp -r [local_path] [user]@[server]:[server_path]
```

git

- clone
```
git clone [git_url]
```

- branch
```
git branch [-r] (-r : remote branch)
git branch [branch_name] (create branch)
git checkout -b [branch_name] (create branch and checkout it)
git branch -d [branch_name] (delete branch)
git merge [branch_name] (merge [branch_name] to now branch)
git push origin [branch_name] (push branch to remote)
```

- log
```
git log --oneline
```

- reset
```
git reset [git_id]
```

## Linux and OSX

- 进程查询
```
ps aux | grep [process_name]
ps -ef  | grep [process_name]
```

- 指令履历
```
history
history | grep [command]
```

- 强制结束进程
```
kill [PID]
kill -9 [PID] ※danger
```

## Windows

