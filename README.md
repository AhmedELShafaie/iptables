# iptables
#Syntax
iptables -t ${table}(nat,filter,mangle) -A(ppend) $(chain)[INPUT,FORWARD,OUTPUT] -i(nterface)(lo,eth0)   
-p(rotocal)(tcp,udp) -dport(destination_port) -s(ource) (Source Address) -j(target)(ACCEPT,DROP,RETURN)    

#-t(filter) is default  
#https://kkslinuxinfo.wordpress.com/2016/02/16/iptables-firewall-tables/  
iptables -A INPUT -i eth0 -p tcp -dport 80 -s any -j ACCEPT  



#Accept traffic lo interface  
iptables -A INPUT -i lo -j ACCEPT  
iptables -L -v  
