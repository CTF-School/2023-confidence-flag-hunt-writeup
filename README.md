# CONFidence 2023 Flaghunt Writeup

### Flag 1 -   CONFIDENCE{the_one_that_is_an_easy_catch}

Hidden in the title of the website.

### Flag 2 -CONFIDENCE{the_one_ncoded_at_the_bottom_of_the_csseee}

Hidden in the assets/style.css. Need to scroll it down and decode it from NATO aplhabet code.

### Flag 3 -  CONFIDENCE{the_one_that_was_online_even_before_the_contest_started}

Hidden on one of the linked website. In the description of CTF School channel.

### Flag 4 -   CONFIDENCE{the_one_thats_on_the_sheeeeep}

Hidden under stacked background, but visible when you open assets/bg.png file.

### Flag 5 -   CONFIDENCE{the_one_thats_inside_the_sheeeeeeeeeeeeep}

Hidden inside assets/sheep.png file, visible when opened as text file.

### Flag 6 -   CONFIDENCE{the_one_from_a_grumpy_admin}

Hidden inside the API page under /api URL. There is an email address to reach the support. When written to it responds with a flag.

### Flag 7 -   CONFIDENCE{the_one_u_can_find_in_a_header}

Hidden in the header named "token" returned with basically every server response. Token needs to be decoded using JWT debugger to get the flag.

### Flag 8 -   CONFIDENCE{the_one_on_api_page}

Hidden inside the API page under /api URL. The API URL was easy to find using any enumeration tool like dirb. API page contains a list of URLs for other challenges.

### Flag 9 -   CONFIDENCE{the_one_on_the_version_2_api_page}

Hidden inside the API under /api/v2 URL. Easy to get with further enumeration or when suggested by the current API version displayed in json file.

### Flag 10 -   CONFIDENCE{the_one_when_you_patch_the_version}

Hidden in the API under /api/version URL. Revealed when the HTTP request is made with a PATCH method.

### Flag 11 -   CONFIDENCE{the_one_when_you_will_get_one_letter_at_the_time}

Hidden in the API under /api/flag URL. When prefix query parameter is provided it will return next letter of a flag that is right after the provided prefix. Starting with C, then CO, CON and so on it will return next letters of a flag.

### Flag 12 -   CONFIDENCE{the_one_on_you_get_when_you_bruuuteforce_my_password}

Hidden in the API under /api/hash URL. When trying to provide password query parameter we can get validation errors showing that the password needs to be lowercase letters and no longer than 10 characters. When any password provided it shows the correct password hash that needs to be bruteforced.

(NOTE: due to my wrong estimation how long this will take to bruteforce on a normal laptop some contestants used cloud services to bruteforce it) 

### Flag 13 -   CONFIDENCE{the_one_on_you_get_when_you_generate_secret_ot_token}

Hidden in the API under /api/totp URL. When entered without a code it shows an error message pointing to params.json file. Entering /api/totp/params.json shows TOTP token secret and parameters allowing to generate the code using any authenticator tool.

### Flag 14 -  CONFIDENCE{the_one_if_you_look_into_my_favourite_icon}

Hidden under /favicon.ico URL, but visible only when entered directly without Referrer header.

### Flag 15 -  CONFIDENCE{the_one_when_you_figure_xor_is_not_good_enough}

Hidden in the API under /api/secret URL. Providing a secret parameter we can get a flag xored with it. This kind of encyrption can be easily reversed, in example passing long string made of "a" characters as a secret, and then xoring the result using "a" as a xor key. 

### Flag 16 -  CONFIDENCE{the_one_on_the_og_img_server}

Hidden on the linked server providing og:image residing here https://ogimgserver.vercel.app. When entered directly it shows apache error page, but looking into the source of flag can be found hidden in a comment.
