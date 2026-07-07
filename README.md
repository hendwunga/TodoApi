# Error saat trust certs
- endos@endos:~/Desktop/TodoApi$ dotnet dev-certs https --trust
- Response:
```
Trusting the HTTPS development certificate was requested. Trust is per-user and may require additional configuration. See https://aka.ms/dev-certs-trust for more information.
There was an error trusting the HTTPS developer certificate. It will be trusted by some clients but not by others.
```

- Solution: 
```
sudo apt update
sudo apt install libnss3-tools
dotnet dev-certs https --trust
dotnet watch 
```

