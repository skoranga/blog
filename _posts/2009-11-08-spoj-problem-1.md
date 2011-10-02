--- 
layout: post
title: SPOJ Problem 1
tags: 
- bash
- c++
- c99
- java
- pascal
- perl
- php
- prime
- python
- ruby
- SPOJ
status: publish
type: post
published: true
meta: 
  _edit_lock: "1258154416"
  _edit_last: "1"
---
When I saw that Thor had done solutions to the first few problems of Project Euler in many many languages, I thought "Hey! That's a good idea!" but didn't want to copy exactly.

So instead I'm doing solutions to some problems on SPOJ.
SPOJ is an online judge system full of algorithmic problems. This is one of the things that <a href="http://www.topcoder.com/tc?module=MemberProfile&cr=22664055&tab=hs">Hanson Wang</a> did to get as good as he is. The solutions I'll be providing here are going to be very simple problems, so don't expect any magic. The beautiful thing about SPOJ is the sheer number of languages it will judge. I figured this was the perfect playground to make sure my code worked in all the languages I try.

Problem: <a href="http://www.spoj.pl/problems/TEST/"> Life, the Universe, and Everything</a>

<blockquote>
Your program is to use the brute-force approach in order to find the Answer to Life, the Universe, and Everything. More precisely... rewrite small numbers from input to output. Stop processing input after reading in the number 42. All numbers at input are integers of one or two digits.
</blockquote>
Solutions - In order of frequency that I use the language

<strong>C++</strong>
<pre LANG='cpp'>
//TEST AC - CPP (g++)
#include <iostream>
using namespace std;

int main() {
	int n;
	while(1) {
		cin >> n;
		if (n == 42) break;
		cout << n << endl;
	}
	return 0;
}
</pre>

<strong>C99</strong>
<pre lang='c'>
//TEST AC - (gcc C99)
#include <stdio.h>
int main() {
	int n;
	while(1) {
		scanf("%d",&n);
		if (n == 42) break;
		printf("%d\n",n);
	}
	return 0;
}
</pre>

<strong>php</strong>
<pre lang='php'>
<?
//TEST AC - PHP
while(1) {
	fscanf(STDIN,"%d",$n);
	if ($n == 42) break;
	print "$n\n";
}
?>
</pre>

<strong>Python</strong>
<pre lang='python'>
#TEST AC - Python
while 1:
	num = input()
	if (num == 42):
		break
	print num
</pre>

<strong>Bash</strong>
<pre lang='bash'>
#!/bin/bash
# TEST AC - BASH

while true; do
	read n
	if [ $n -eq 42 ]; then
		break
	fi
	echo "$n"
done
</pre>

<strong>Ruby</strong>
<pre lang="ruby">
#TEST AC - Ruby
while 1
	n = gets.to_i
	if n == 42
		break
	end
	puts n
end
</pre>

<strong>Java</strong>
<pre lang='java'>
//TEST AC - Java
import java.io.*;
import java.util.*;

public class Main {
	public static void main(String[] args) {
		Scanner in = new Scanner(System.in);

		while(true) {
			int n = in.nextInt();
			if (n == 42) break;
			System.out.println(n);
		}
	}
}
</pre>

<strong>Perl</strong>
<pre lang='perl'>
#TEST AC - Perl
while (1)
{
	$n = <STDIN>;
	if ($n == 42) {
		last;
	}
	print $n
}
</pre>

<strong>C#</strong>
<pre lang='csharp'>
//TEST AC - C# (gmcs + Mono)
using System;
class WelcomeCSS {
	static void Main() {
		while(true) {
			int n;
			n = int.Parse(Console.ReadLine());
			if (n == 42) break;
			Console.WriteLine(n);
		}
	}
}
</pre>

<strong>GNU Pascal</strong>
<pre lang='pascal'>
{TEST AC - GPC Pascal}

program TEST;

var n:integer;

begin
	while true do
		begin
			readln(n);
			if n = 42 then begin
				break;
			end;
			writeln(n);
		end;
end.
</pre>

You can see Thor's Project Euler solutions here: <a href="http://www.thurn.ca/category/project-euler/">Derek Thurn's Website - Project Euler</a>