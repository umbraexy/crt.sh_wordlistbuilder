#!/bin/sh 
#3/24/2023
#Created by umbraexy


read -p "Enter the domain to build a wordlist from:" domainaddr;
curl "https://crt.sh/?q=$domainaddr" | grep -i $domainaddr | sort -u > $domainaddr.wordlist 2> /dev/null;
sed -i 's/<TD>\|<\/TD>$//g' $domainaddr.wordlist 2> /dev/null;
sed -i 's/ *//g' $domainaddr.wordlist 2>/dev/null;
sed -i '/^[^[:alnum:]]/d' $domainaddr.wordlist 2>/dev/null;
sed -i 's/<BR>/\n/g' $domainaddr.wordlist 2>/dev/null;
sort -u $domainaddr.wordlist -o $domainaddr.wordlist;

