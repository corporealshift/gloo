<!-- Code generated by solo-kit. DO NOT EDIT. -->

### Package: `gloo.solo.io` 
##### Types:


- [ListenerPlugins](#ListenerPlugins)
- [VirtualHostPlugins](#VirtualHostPlugins)
- [RoutePlugins](#RoutePlugins)
- [DestinationSpec](#DestinationSpec)
- [UpstreamSpec](#UpstreamSpec)
  



##### Source File: [github.com/solo-io/gloo/projects/gloo/api/v1/plugins.proto](https://github.com/solo-io/gloo/blob/master/projects/gloo/api/v1/plugins.proto)





---
### <a name="ListenerPlugins">ListenerPlugins</a>

 
Plugin-specific configuration that lives on listeners
Each ListenerPlugin object contains configuration for a specific plugin
Note to developers: new Listener Plugins must be added to this struct
to be usable by Gloo.

```yaml

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 




---
### <a name="VirtualHostPlugins">VirtualHostPlugins</a>

 
Plugin-specific configuration that lives on virtual hosts
Each VirtualHostPlugin object contains configuration for a specific plugin
Note to developers: new Virtual Host Plugins must be added to this struct
to be usable by Gloo.

```yaml
"extensions": .gloo.solo.io.Extensions

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `extensions` | [.gloo.solo.io.Extensions](extensions.proto.sk.md#Extensions) |  |  |




---
### <a name="RoutePlugins">RoutePlugins</a>

 
Plugin-specific configuration that lives on routes
Each RoutePlugin object contains configuration for a specific plugin
Note to developers: new Route Plugins must be added to this struct
to be usable by Gloo.

```yaml
"transformations": .transformation.plugins.gloo.solo.io.RouteTransformations
"faults": .fault.plugins.gloo.solo.io.RouteFaults
"prefix_rewrite": .transformation.plugins.gloo.solo.io.PrefixRewrite
"timeout": .google.protobuf.Duration
"retries": .retries.plugins.gloo.solo.io.RetryPolicy
"extensions": .gloo.solo.io.Extensions

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `transformations` | [.transformation.plugins.gloo.solo.io.RouteTransformations](plugins/transformation/transformation.proto.sk.md#RouteTransformations) |  |  |
| `faults` | [.fault.plugins.gloo.solo.io.RouteFaults](plugins/faultinjection/fault.proto.sk.md#RouteFaults) |  |  |
| `prefix_rewrite` | [.transformation.plugins.gloo.solo.io.PrefixRewrite](plugins/transformation/prefix_rewrite.proto.sk.md#PrefixRewrite) |  |  |
| `timeout` | [.google.protobuf.Duration](https://developers.google.com/protocol-buffers/docs/reference/csharp/class/google/protobuf/well-known-types/duration) |  |  |
| `retries` | [.retries.plugins.gloo.solo.io.RetryPolicy](plugins/retries/retries.proto.sk.md#RetryPolicy) |  |  |
| `extensions` | [.gloo.solo.io.Extensions](extensions.proto.sk.md#Extensions) |  |  |




---
### <a name="DestinationSpec">DestinationSpec</a>

 
Configuration for Destinations that are tied to the UpstreamSpec or ServiceSpec on that destination

```yaml
"aws": .aws.plugins.gloo.solo.io.DestinationSpec
"azure": .azure.plugins.gloo.solo.io.DestinationSpec
"rest": .rest.plugins.gloo.solo.io.DestinationSpec
"grpc": .grpc.plugins.gloo.solo.io.DestinationSpec
"sqoop": .sqoop.plugins.gloo.solo.io.DestinationSpec

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `aws` | [.aws.plugins.gloo.solo.io.DestinationSpec](plugins/aws/aws.proto.sk.md#DestinationSpec) |  |  |
| `azure` | [.azure.plugins.gloo.solo.io.DestinationSpec](plugins/azure/azure.proto.sk.md#DestinationSpec) |  |  |
| `rest` | [.rest.plugins.gloo.solo.io.DestinationSpec](plugins/rest/rest.proto.sk.md#DestinationSpec) |  |  |
| `grpc` | [.grpc.plugins.gloo.solo.io.DestinationSpec](plugins/grpc/grpc.proto.sk.md#DestinationSpec) |  |  |
| `sqoop` | [.sqoop.plugins.gloo.solo.io.DestinationSpec](plugins/sqoop/sqoop.proto.sk.md#DestinationSpec) |  |  |




---
### <a name="UpstreamSpec">UpstreamSpec</a>

 
Each upstream in Gloo has a type. Supported types include `static`, `kubernetes`, `aws`, `consul`, and more.
Each upstream type is handled by a corresponding Gloo plugin.

```yaml
"kube": .kubernetes.plugins.gloo.solo.io.UpstreamSpec
"static": .static.plugins.gloo.solo.io.UpstreamSpec
"aws": .aws.plugins.gloo.solo.io.UpstreamSpec
"azure": .azure.plugins.gloo.solo.io.UpstreamSpec
"consul": .consul.plugins.gloo.solo.io.UpstreamSpec

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `kube` | [.kubernetes.plugins.gloo.solo.io.UpstreamSpec](plugins/kubernetes/kubernetes.proto.sk.md#UpstreamSpec) |  |  |
| `static` | [.static.plugins.gloo.solo.io.UpstreamSpec](plugins/static/static.proto.sk.md#UpstreamSpec) |  |  |
| `aws` | [.aws.plugins.gloo.solo.io.UpstreamSpec](plugins/aws/aws.proto.sk.md#UpstreamSpec) |  |  |
| `azure` | [.azure.plugins.gloo.solo.io.UpstreamSpec](plugins/azure/azure.proto.sk.md#UpstreamSpec) |  |  |
| `consul` | [.consul.plugins.gloo.solo.io.UpstreamSpec](plugins/consul/consul.proto.sk.md#UpstreamSpec) |  |  |





<!-- Start of HubSpot Embed Code -->
<script type="text/javascript" id="hs-script-loader" async defer src="//js.hs-scripts.com/5130874.js"></script>
<!-- End of HubSpot Embed Code -->