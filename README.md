# Parser
Parser

The parser for url, ipv4 and ipv6

#url
def printParsed(text, regex, desc):
  try:
    _list = re.findall(regex, text)
		  for item in _list:
			  item = item.lower()
			  print(desc, item)
			
	except Exception as e:
		print(str(e))

			
def main():
  f = file.open(myfile.txt)
  text = str(f.read())
  
  #url
  regex_url = = r'(?:[a-zA-Z0-9](?:[a-zA-Z0-9\-]{,61}[a-zA-Z0-9])?\.)+[a-zA-Z]{2,6}'
  printParsed(text, regex_url, "url")
  
  #prefix
  regex_prefix = = r'(?:\d{1,3}\.){3}\d{1,3}/\d{1,2}'
  printParsed(text, regex_prefix, "prefix")

  #ip
  regex_ip = r'(?:[\d]{1,3})\.(?:[\d]{1,3})\.(?:[\d]{1,3})\.(?:[\d]{1,3})'
  printParsed(text, regex_ip, "ip")



