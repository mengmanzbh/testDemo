docker run -it --rm erlang /bin/bash
- docker system prune

删除所有镜像

- docker rmi $(docker images -q)

杀死所有正在运行的容器
- docker kill $(docker ps -a -q)
删除所有已经停止的容器
- docker rm $(docker ps -a -q)
删除所有未打 dangling 标签的镜像
c docker rmi $(docker images -q -f dangling=true)


https://portswigger.net/burp/communitydownload
https://www.paterva.com/web7/community/community.php
https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#







docker run --name chiaok -v /temp:/temp -d ghcr.io/chia-network/chia:latest

docker run --net=host -v /run/media/yangmi/chia:/temp -d ghcr.io/chia-network/chia:latest


docker exec -it chiaok venv/bin/chia plots create -k 32 -f b7be10ac7eb05fbf27af6153606f5ff5469141fd5417aaa8fa3b225cc8d41a6ab986749e5a50ea09b502777b47d0c6a4 -p a541438b8f42e99666bdfa3a7fbf89b6cfdc9878ece814b4a2256fcce144896b5360d8670da323db8236440cd6d4f1eb -b 15000 -r 8 -u 128 --exclude_final_dir -t /temp -d /temp
