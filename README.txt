docker build -t="grassa/apache" .
docker run -d -p 80:80 --name=servweb grassa/apache
