<h1 align="center">
<a href="myrepository"><img src="https://user-images.githubusercontent.com/60064250/146137115-d87b60fa-fd7c-46f7-9efd-9fc95845f47c.png" alt="NSR"></a>
<br>
👑 NSR 👑
</h1>
<p align="center">
	
</p>

The step of recognizing a target in both Bug Bounties and Pentest can be very time-consuming. Thinking about it, I decided to create my own recognition script with all the tools I use most in this step.
All construction of this framework is based on the methodologies of [@Jhaddix](https://twitter.com/Jhaddix). These people were my biggest inspirations to start my career in Information Security and I recommend that you take a look at their content, you will learn a lot!<br>


## Help menu 🔎

Option     		 | Value
---        		 | ---       
-h, --help 		 | `Look at the complete help menu`
-d       		 | `domain.com`
-w     		     | `Path to your wordlist. Some wordlists I've already added by default to ./wordlists`
-f				 | `Fuzzing mode. When passing this argument, the Fuzzing step to confirm possible vulnerabilities will be added. Directory Fuzzing will remain enabled regardless of whether the argument is passed or not. I recommend not to use this if you want to do a recon faster.`
-g      		 | `GitHub API Key. This parameter is used when searching for subdomains`
-s       		 | `Shodan API Key. This parameter is used to automate the search for domains associated with your target(Requires API Key premium). If you don't have it, you can do the searches manually and the dorks are saved in the output folder.`
-o     		     | `Your output folder. If you don't specify the parameter, all the results of the script will be saved in a folder with your target's name inside the script path`
-q       		 | `Quiet mode. All banners and details of the script's execution will not be shown in the terminal, but everything that is executed in normal mode is executed as well. You will be able to see all the results in detail in your output folder`


## Usage 💡

![Help Menu](https://helpdemo page)
### Basic usage
```
❯ ./nsr.sh -d domain.com -w /path/to/your/wordlist.txt
```
### Quiet mode
```
❯ ./nsr.sh -d domain.com -w /path/to/your/wordlist.txt -q
```
### Recommended usage
```
❯ ./nsr.sh -d domain.com -w /path/to/your/wordlist.txt -g [github_api_key] -s [shodan_api_key] -f
```
![Usage](https://workinggifphoto)


## Features ✅
### ASN Enumeration
- [metabigor](https://github.com/j3ssie/metabigor)
### Subdomain Enumeation
- [Assetfinder](https://github.com/tomnomnom/assetfinder)
- [Subfinder](https://github.com/projectdiscovery/subfinder)
- [Amass](https://github.com/OWASP/Amass)
- [Findomain](https://github.com/Findomain/Findomain)
- [Sublist3r](https://github.com/aboul3la/Sublist3r)
- [Knock](https://github.com/guelfoweb/knock)
- [SubDomainizer](https://github.com/nsonaniya2010/SubDomainizer)
- [GitHub Sudomains](https://github.com/gwen001/github-search/blob/master/github-subdomains.py)
- [RapidDNS](https://rapiddns.io/)
- [Riddler](https://riddler.io/)
- [SecurityTrails](https://securitytrails.com/)
### Alive Domains
- [httprobe](https://github.com/tomnomnom/httprobe)
- [httpx](https://github.com/projectdiscovery/httpx)
### WAF Detect
- [wafw00f](https://github.com/EnableSecurity/wafw00f)
### Domain organization
- Regular expressions
### Subdomain Takeover
- [Subjack](https://github.com/haccer/subjack)
### DNS Lookup
#### Discovering IPs
- [dnsx](https://github.com/projectdiscovery/dnsx)
#### DNS Enumeration and Zone Transfer
- [dnsrecon](https://github.com/darkoperator/dnsrecon)
- [dnsenum](https://github.com/fwaeytens/dnsenum)
### Favicon Analysis
- [favfreak](https://github.com/devanshbatham/FavFreak)
- [Shodan](https://www.shodan.io/)
### Directory Fuzzing
- [ffuf](https://github.com/ffuf/ffuf)
### Google Hacking
- Some Dorks that I consider important
- [CredStuff-Auxiliary](https://github.com/pedr4uz/CredStuff-Auxiliary)
- [Googler](https://github.com/jarun/googler)
### GitHub Dorks
- [Jhaddix Dorks](https://gist.github.com/jhaddix/1fb7ab2409ab579178d2a79959909b33)
### Credential Stuffing
- [CredStuff-Auxiliary](https://github.com/pedr4uz/CredStuff-Auxiliary)
### Screenshots
- [EyeWitness](https://github.com/FortyNorthSecurity/EyeWitness)
### Port Scan
- [Masscan](https://github.com/robertdavidgraham/masscan)
- [Nmap](https://github.com/nmap/nmap)
- [Naabu](https://github.com/projectdiscovery/naabu)
### Link Discovery
#### Endpoints Enumeration and Finding JS files
- [Hakrawler](https://github.com/hakluke/hakrawler)
- [Waybackurls](https://github.com/tomnomnom/waybackurls)
- [Gospider](https://github.com/jaeles-project/gospider)
- [ParamSpider](https://github.com/devanshbatham/ParamSpider)
### Vulnerabilities
- [Nuclei](https://github.com/projectdiscovery/nuclei) **➔ I used all the default templates**
#### 403 Forbidden Bypass
- [Bypass-403](https://github.com/iamj0ker/bypass-403)
#### XSS
- [XSStrike](https://github.com/s0md3v/XSStrike)
- [Gxss](https://github.com/KathanP19/Gxss)
#### LFI
- Oneliners
	- [gf](https://github.com/tomnomnom/gf)
	- [ffuf](https://github.com/ffuf/ffuf)
#### RCE
- My GrepVuln function
#### Open Redirect
- My GrepVuln function
#### SQLi
- Oneliners
	- [gf](https://github.com/tomnomnom/gf) 
	- [sqlmap](https://github.com/sqlmapproject/sqlmap)
## Installation
I made a script that automates the installation of all tools. I tried to do it with the intention of having compatibility with the most used systems in Pentest and Bug Bounty.
```
git clone https://github.com/dirsoooo/Recon.git
cd Recon/
chmod +x recon.sh
chmod +x installation.sh
./installation.sh
```
**Please DO NOT remove any of the files inside the folder, they are all important!**
### Installation script tested on:
- Kali Linux <br>[<img width="100px" src="https://lcom.static.linuxfound.org/images/stories/66866/kali-logo.png">](https://www.kali.org/)
## Poject Mindmap

![Mindmap](https://user-images.githubusercontent.com/60064250/146136303-2d61abe9-a360-4c24-9f9e-f07fcef77016.png)

## License
``NSR`` was entirely coded with ❤ by [@TeamNSR] and it is released under the MIT license.

