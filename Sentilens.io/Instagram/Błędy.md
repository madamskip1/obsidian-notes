## Nieaktualny klucz

```
Traceback (most recent call last):
  File "/home/maciej/Repozytoria/sentilens.io/backend/instagram_app/simple_script_get_comments.py", line 33, in <module>
    main()
  File "/home/maciej/Repozytoria/sentilens.io/backend/instagram_app/simple_script_get_comments.py", line 14, in main
    media_list = instagram_api_client.get_user_media_list()
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/maciej/Repozytoria/sentilens.io/backend/instagram_app/api_client.py", line 20, in get_user_media_list
    response_data = self.__send_request_and_get_data_response(endpoint)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/maciej/Repozytoria/sentilens.io/backend/instagram_app/api_client.py", line 70, in __send_request_and_get_data_response
    response = self.__send_request_and_get_response(endpoint)
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/maciej/Repozytoria/sentilens.io/backend/instagram_app/api_client.py", line 62, in __send_request_and_get_response
    raise requests.RequestException(
requests.exceptions.RequestException: Error fetching Instagram API data: Error validating access token: The session has been invalidated because the user changed their password or Facebook has changed the session for security reasons.
[1]    8543 exit 1     python3 simple_script_get_comments.py
```

[https://developers.facebook.com/docs/instagram-platform/reference/refresh_access_token](https://developers.facebook.com/docs/instagram-platform/reference/refresh_access_token "https://developers.facebook.com/docs/instagram-platform/reference/refresh_access_token")

