Welcome to Linux for Devops!!!

    This Repository created for easy way of understanding of linux commands that every Devops Engineer uses on their daily assignment of work like creating user/directoories , file/folder permissions, log monitoring or log checks on instances, directory sturcture on linux.

    It will give basic idea of linux commands that enterining into the software field on any role.

1. Basic Linux Commands

pwd – Print Working Directory


📌 Shows the current directory path.

ls – List Files & Directories
ls
ls -l
ls -a
ls -lh


-l → long format

-a → hidden files

-h → human readable sizes

🛠 DevOps Use: Checking logs, configs, artifacts.

cd – Change Directory
cd /var/log
cd ..
cd ~

📌 2. File & Directory Management (Very Important)
mkdir – Create Directory
mkdir devops
mkdir -p project/app/logs

touch – Create Empty File
touch app.log

cp – Copy Files
cp file1.txt file2.txt
cp -r app/ backup/

mv – Move / Rename
mv oldname.txt newname.txt

rm – Delete Files
rm file.txt
rm -rf directory/


⚠️ Danger: rm -rf / can destroy the system.

📌 3. Viewing & Analyzing Files (Logs!)
cat
cat app.log

less / more
less /var/log/syslog

head / tail
head -n 10 app.log
tail -n 20 app.log
tail -f app.log


🛠 DevOps Use: Live log monitoring.

📌 4. Searching & Filtering (Critical Skill)
grep
grep "ERROR" app.log
grep -i "failed" app.log

find
find /var -name "*.log"
find . -size +100M

awk
awk '{print $1}' file.txt

sed
sed 's/ERROR/WARNING/g' app.log

📌 5. Permissions & Ownership (Must Know)
chmod
chmod 777 file.sh
chmod +x script.sh

Permission	Meaning
r	read
w	write
x	execute
chown
chown user:user file.txt

📌 6. User & Group Management
useradd devops
passwd devops
groupadd admin
usermod -aG admin devops


🛠 DevOps Use: Managing access on servers.

📌 7. Process Management
ps
ps -ef

top / htop
top

kill
kill 1234
kill -9 1234

📌 8. Disk & Memory Monitoring
df -h
du -sh /var/log
free -m


🛠 DevOps Use: Server health checks.

📌 9. Networking Commands
ip a
ping google.com
netstat -tulnp
ss -tulnp
curl http://localhost:8080
wget https://example.com/file.zip

📌 10. Package Management (Ubuntu)
apt update
apt install nginx -y
apt remove nginx

📌 11. Services & Systemctl
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl status nginx
systemctl enable nginx


🛠 DevOps Use: Managing applications & services.

📌 12. Archive & Compression
tar -cvf backup.tar app/
tar -xvf backup.tar
gzip file.txt
gunzip file.txt.gz

📌 13. Environment Variables
export ENV=production
echo $ENV

📌 14. Shell Scripting Basics
#!/bin/bash
echo "Hello DevOps"
date
uptime


Make executable:

chmod +x script.sh
./script.sh

📌 15. DevOps Practical Scenarios
🔹 Monitor Logs
tail -f /var/log/nginx/access.log

🔹 Find High Disk Usage
du -ah / | sort -rh | head -10

🔹 Kill High CPU Process
top
kill -9 PID