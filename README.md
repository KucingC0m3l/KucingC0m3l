```text
              .:+:.                     Name        : Shahrul Nizam
            .#@+                        Handle      : @BroNiz4m
           +@@+                         Mostly into : Security research
          +@@@                                        Systems & hardware
         .@@@@                          CVEs        : 3 officially assigned
  ..     .@@@@+                         Right now   : Probably sleeping.
          #@@@@+                        
            +#@@@@@#++:::+##:     .
              :+#@@@@@@##+.
                   ...

             .+###@#+:
             :@@@@@@#:.
             .#@@@@#
              +@@@@#:        :
             .#@@@@@@:
           +#@@@@@@@@:
    ..   :#@@@@@@@@@#
  +#:.  .#@@@@@@@@@#
 :@.    #@@@@@@@##@+
 :@.    #@@@@@@@@#@:
  +#:   :@@@@@@@#:#+
   .+##+#@@@@@@@####+..
 ..::..:.................:...
```

```bash
broniz4m@github:~$ sed 's/^/# /' ~/profile/about.md

# Most things here started because I got curious and kept digging.
#
# Sometimes it's a broken laptop, sometimes a web bug,
# and sometimes a small idea that refuses to stay small.
#
# I test things, trace what happened, and write down the useful
# parts before I forget them.


broniz4m@github:~$ cd ~/CVE-Disclosures/CVE-2026

broniz4m@github:~/CVE-Disclosures/CVE-2026$ find . -maxdepth 1 -mindepth 1 -type d -name 'CVE-*' -printf '%f\n' | sort

CVE-2026-63081
CVE-2026-63082
CVE-2026-64829


broniz4m@github:~/CVE-Disclosures/CVE-2026$ for file in CVE-*/README.md; do
>   sed -n '1s/^# //p' "$file" | fold -s -w 72
>   echo
> done

CVE-2026-63081 - Perfect Support Ticketing System 1.7 Stored XSS via Ticket Notes Field

CVE-2026-63082 - Perfect Support Ticketing System 1.7 Broken Access Control via Agent Assignment

CVE-2026-64829 - Question2Answer 1.8.8 Session Fixation via Forgot-Password Flow


broniz4m@github:~/CVE-Disclosures/CVE-2026$ cd ~

```
