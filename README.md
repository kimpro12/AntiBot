Feature: 
- Add ipset to antibot
- Before using this scipt the cps of spambot always higher like this:
- ![image](https://user-images.githubusercontent.com/95573884/156032045-208207e8-5203-43bc-a607-1449579728b7.png)
- After using script cps is always 100-200 cps even you have the spambot 100k cps:
- ![Annotation 2022-03-01 002847](https://user-images.githubusercontent.com/95573884/156032300-e50d1b49-6451-4eca-82d9-03019f2ee9e7.png)
- The operating principle is i blacklist a lot of proxy around the world to Antibot.
- It blacklist more than 120k proxy online.

How to use:
- Copy Paste this command 
- sudo echo "pls run this scipt on root" && sudo apt -y install ipset && sudo apt install curl && sudo curl -o blacklist.txt https://raw.githubusercontent.com/kimpro12/MCBOT/main/blacklist.txt && sudo ipset destroy blacklist ; sudo ipset restore -! < blacklist.txt ; sudo rm blacklist.txt && sudo iptables -D INPUT -m set --match-set blacklist src -j DROP ; sudo iptables -I INPUT -m set --match-set blacklist src -j DROP && sudo echo "done.Thank for using this scipt this scipt made by fip"

- Or download run.sh and use command sudo sh run.sh

- If you see some error logs like this,don't care this:

![image](https://user-images.githubusercontent.com/95573884/159100121-498b348e-186a-485a-885e-e140c93812a9.png)



Enjoy !!
