bindhost(){
    
  sudo ifconfig lo0 "$1" alias
  echo "rdr pass on lo0 inet proto tcp from any to $1 port 80 -> 127.0.0.1 port $2" |
  sudo pfctl -ef - | 
  echo "$1"    "$3" |
  sudo tee -a /etc/hosts | 
  sudo dscacheutil -flushcache

}
