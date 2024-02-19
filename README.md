# Welcome to the DataOps Jedi Challenge!

Greetings, brave Data Jedis! Prepare your lightsabers and channel the Force as you embark on a thrilling adventure through the data galaxy. In this challenge, you'll wield your data mastery to ingest, parse, and uncover hidden flags scattered across the stars.

## Prerequisites 

Before embarking on this epic quest, ensure you have the following prerequisites:

- **Curl:** Equipped with this tool, you'll be ready to interact with APIs like a true Jedi.

## May the Flags Be With You

As you traverse the data galaxy, keep an eye out for the following flags:

1. **Test a Parser**: Let your Jedi instincts guide you as you test your parsing skills.
2. **Create a Dashboard**: Craft a dashboard worthy of the Jedi Council to showcase your triumphs. 
3. **Click Flags you Parsed**: Unveil the hidden flags and claim your rightful place among the data elite. (see below)

## Parsing Flags - Your Jedi Trials

In this exercise, you'll face your Jedi trials:

1. **Send Some Data Over**: Use your command over the Force to send data through the data pipeline. May the timestamps be in your favor!
  
```bash
curl --location 'https://xdr.us1.sentinelone.net/api/addEvents' \\
--header 'Content-Type: application/json' \\ 
--header 'Cookie: sp=35eb6acb-d6cf-488d-a0ab-215e637e27db' \\
--data '{"token": "token-provided-on-data-ops-day", "session": "session_{{random_number}}", "sessionInfo": {"serverHost": "sko25", "logfile": "sko25"}, "events": [{"ts": "'$(($(date +%s%N) - 5*60*60*1000000000))'", "attrs": {"message": "{\"flag\":\"BB8-'$USER'\", \"description\": \"these are the droids you\''re looking for\", \"User\": \""${USER/@*}"\"}", "parser": "sko25-"'${USER/@*}'"}}, {"ts": "'$(($(date +%s%N)))'", "attrs": {"message": "user=\'"$USER"\',flag=R2D2-'$USER',description=These are the droids you\''re looking for,code=200", "parser": "sko25-"'${USER/@*}'", "field 1": "x", "field 2": "y"}}]}'  
```

2. **Find the Unparsed Data**: Your Jedi senses will guide you to the unparsed data. Seek, and you shall find!

3. **Apply a Parser**: With the wisdom of Yoda, apply the JSON parser to unlock the secrets hidden within the data.

4. **Click the "Flag" to Go on the Leaderboard**: Prove your worth by clicking the "Flag" and ascending to the ranks of the Jedi Masters.

5. **Click the First Flag**: Encounter friendly droids and unlock the mysteries of the Force.


**Ready to Embark on Your Journey?**
------------------------------------  

With these instructions in hand, embark on your DataOps Jedi journey and may the flags be with you, always! 🌌✨

Feel free to copy and paste this markdown into your editor for a whimsical DataOps adventure!
