Metagoofil
==========

This is an unofficial fork of Metagoofil by Edge Security

What is this?
-------------

Metagoofil is a tool for extracting metadata of public documents (pdf,doc,xls,ppt,etc) availables in the target websites.This information could be useful because you can get valid usernames, people names, for using later in bruteforce password attacks (vpn, ftp, webapps), the tool will also extracts interesting "paths" of the documents, where we can get shared resources names, server names, etc.

This new version will also extract emails addresses from PDF and Word documents content.

How it works?
-------------

The tool first perform a query in Google requesting different filetypes that can have useful metadata (pdf, doc, xls,ppt,etc), then will download those documents to the disk and extracts the metadata of the file using specific libraries for parsing different file types (Hachoir, Pdfminer, etc)


Dependencies:
-------------
Python2

Usage
-----
	-d: domain to search
	-t: filetype to download (pdf,doc,xls,ppt,odp,ods,docx,xlsx,pptx)
	-l: limit of results to search (default 200)
	-h: work with documents in directory (use "yes" for local analysis)
	-n: limit of files to download
	-o: working directory (location to save downloaded files)
	-f: output file

	Examples:
		metagoofil.py -d apple.com -t doc,pdf -l 200 -n 50 -o applefiles -f results.html
		metagoofil.py -h yes -o applefiles -f results.html (local dir analysis)
