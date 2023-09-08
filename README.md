##you must install a linux distro to your wsl2 .
\\wsl.localhost\void\mnt

docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/mnt/Docker:/app" -v /app/node_modules feedback-node:volumes

docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/mnt/Docker/data-volumes:/app:ro" -v /app/temp -v /app/node_modules
 feedback-node:volumes