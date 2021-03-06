# API created following the [Tutorial: Create a web API with ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-6.0&tabs=visual-studio)

Using a DB mock that saves in-memory data for the present moment (will change for a Mongo or relational DB later)  

## Testing

To test the API I'm using the [http-repl](https://docs.microsoft.com/en-us/aspnet/core/web-api/http-repl/?view=aspnetcore-6.0&tabs=windows).

- To connect
```
httprepl https://localhost:<PORT>/api/todoitems
```

- POST
```
connect https://localhost:<PORT>/api/todoitems
post -h Content-Type=application/json -c "{"name":"walk dog","isComplete":true}"
```

- GET
```
connect https://localhost:<PORT>/api/todoitems
get
```

- GET{:id}
```
connect https://localhost:<PORT>/api/todoitems/{:id}
get
```

- PUT{:id}
```
connect https://localhost:<PORT>/api/todoitems/{:id}
put -h Content-Type=application/json -c "{"id":1,"name":"feed fish","isComplete":true}"
```

- DELETE{:id}
```
connect https://localhost:<PORT>/api/todoitems/{:id}
delete
```

## Future
I intend to transform this little project in something using Angular, Docker and Kubernetes. So this is going to be the back-end associated with an DB application that I'll do later :P