
This shows that foreman/forego will stop completely if one process stops, while supervisord will try to restart the failing service 3 times and then stop trying to restart the service but supervisord will still be running...


