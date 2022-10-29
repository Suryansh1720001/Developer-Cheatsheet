grep
grep -r pattern	find in files
grep -i pattern	ignore case
grep -o pattern	print file:match
grep -h pattern	hide filename
grep -e pattern -e str2	multiples strings
grep -v pattern	compli¬menting line
grep -c pattern	print count
grep -n pattern	print # of matches
grep -w pattern	match whole pattern


find
find path -type f -name file	search only filenames
find path -type d -name dir	search only dir names
find path -mtime +7 -ls	older than 7 days
find path -size -10M -ls	less than 10 MB G/K
find path -exec grep -i str {} +	find in files


du
du -a dir	all files
du -h dir	human
du -m dir	in mb
du -c dir	sum
du -s dir	only sum
du --max-¬depth=1 dir	1 dir level deep


loops
seq 5 | xargs -I{} cmd
for i in {1..5};
do
date;
done
for vm in web log db;
do
uptime;
done


tar
tar cvf f.tar f1 f2 f3 ...	create tar
tar xvf f.tar	extract tar
tar tvf f.tar	view tar


sed
sed -i'.bak' 's/old¬/new/g'	replace after backup
sed 's/ab/¬xy/¬g;s¬/de¬/pq/g'	multiple replaces
sed '10,20 s/abc/¬xyz/g'	replace in range
awk
awk -F',' '{print $1"@¬"$3}'	print col1@col3
awk -F'\t' '/str/ {print $0}'	print line with str
awk -F: '{print $(NF-1)}'	print II col from right
awk -F'(,|¬:|;)' '{print }'	multiple separators
awk '$1 == 100 {print}'	comparison <, >, <=, >=
awk 'END {print NR " & " NF}'	print # of rows and cols
awk 'BEGIN {action} /pattern/ END {action}'


stdin stdout
cmd 1>f.out	stdout to f.out
cmd 1>f.out	stderr to f.out
cmd &>¬f.out	stdout and stderr to f.out


sort
sort -n	numeric
sort -r	reverse


uniq
uniq -c	print count
uniq -d	only dups
uniq -u	only unique
uniq -i	ignore case
ideally uniq should be used after sort


cut
cut -d ',' -f 1,3,5	print csv cols 1, 3 and 5
cut -d: -f 1 --comp¬liment	print all cols except 1
cut -f -3	print cols 1, 2 and 3
cut -f 3-	print cols 3, 4 ...


tr
tr old new	replace old with new
tr -s ' '	replace multiple space with single
typical use: cat something | tr old new


curl
curl -o file url	save to file
curi -I url	only header
curl -k https:¬//url	ignore cert
curl -u <us¬r:p¬wd> url	username password
curl -w	add timeout


misc 1
top	cpu mem info
free -m	mem status
lsof	open files
netstat	nw traffic
dig servername	dns
nslookup servername	dns
time cmd	exe time
watch cmd	auto exe
zip -d f.zip fname	delete file from zip
umount -l mnt	unmount when free
mount -a	mount all
ln -s file link	create symlink


misc 2
| xargs cmd	throws what pipe gave after cmd
ps -ef	list processes
nc -l 1234	listen on 1234
nc 127.0.0.1 1234	send data to 1234
cp -p old new	cp permis¬sions also

