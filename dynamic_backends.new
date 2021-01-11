backend server1 {
    .host = "172.31.0.203";
    .port = "http";
    }

backend server2 {
    .host = "172.31.5.19";
    .port = "http";
    }

sub vcl_init {
    new vdir = directors.round_robin();
    vdir.add_backend(server1);
    vdir.add_backend(server2);
}
