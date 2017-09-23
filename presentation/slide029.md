            ____
           / __ \___  ____ ___  ____
          / / / / _ \/ __ `__ \/ __ \
         / /_/ /  __/ / / / / / /_/ /
        /_____/\___/_/ /_/ /_/\____/

        Using curl ...

        curl -H "Accept: application/json" \
            -H "Content-type: application/json" \
            -X POST -d '{"grant_type":"password","client_id":"<client_id>","username":"<username>","password":"<password>"}' \
            <url>

        curl -H "Accept: application/json" \
            -H "Content-type: application/json" \
            -H "Authorization: Bearer <token>" \
            <url>


        http POST :8000/v1/auth/token grant_type=password client_id=<client_id> username=<username> password=<password>
        http <url> "authorization: Bearer <token>" (and with --session=<name> to save the session)
















































































slide 029
