# New-in-GO-1.8

# HTTP graceful shutdown

It is now possible to call srv.Close() to halt an http.Server immediately, or srv.Shutdown(ctx) to stop and gracefully drain the server of connections.

# HTTP/2.0 server push via http.Pusher

If a web server supports HTTP/2.0, the http.ResponseWriter provided to handlers will also implement the new http.Pusher interface. Handlers can use its functionality to trigger a Server Push for a resource by providing an HTTP method, path, and request headers.

# Changes in database/sql

The database/sql package has several major additions that give more control over database queries and allow users to take advantage of additional database features.

Queries take a context.Context that can be used to cancel queries.
Native database column types are exposed via sql.ColumnType.
Queries can be executed with named parameters if the underlying driver implements support for them.

# Plugins

Plugin support is implemented via the new plugin stdlib package. This will allow Go programs to load additional code—like plugins—while the program is running.

HTTP/2.0 server push via http.Pusher

If a web server supports HTTP/2.0, the http.ResponseWriter provided to handlers will also implement the new http.Pusher interface. Handlers can use its functionality to trigger a Server Push for a resource by providing an HTTP method, path, and request headers.

# Universal slice sorting

It’s implemented via new sort.Slice function. This allows any slice to be sorted by providing a comparator callback rather than creating a specialized sort.Interface implementation.

# TLS additions

Support for ChaCha20-Poly1305 based cipher suites
More flexible config APIs

# Import path of context

Yes, finally.

-import "golang.org/x/next/context"
+import "context"

# Runtime

Some improvements in runtime:

gc pause (< 1ms)
build (15% speedup)
defer (10-35% speedup)
cgo (45% speedup)

# SSA improvements

 20-30% reduction in binary size
 5-35% speedup

# Default $GOPATH

$HOME/go on Unix.

# go bug

Just run go bug and you ill be redirected to a “New Issue” page.
