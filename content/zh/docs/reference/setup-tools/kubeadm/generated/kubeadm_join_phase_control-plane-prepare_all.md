
<!--
### Synopsis
-->
### 概要


<!--
Prepare the machine for serving a control plane
-->
准备为控制平面服务的机器

```
kubeadm join phase control-plane-prepare all [api-server-endpoint] [flags]
```

<!--
### Options
-->
### 选项

<table style="width: 100%; table-layout: fixed;">
  <colgroup>
    <col span="1" style="width: 10px;" />
    <col span="1" />
  </colgroup>
  <tbody>

    <tr>
      <td colspan="2">--apiserver-advertise-address string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      If the node should host a new control plane instance, the IP address the API Server will advertise it's listening on. If not set the default network interface will be used.
      -->
      如果该节点托管一个新的控制平面实例，则 API 服务器将公布其正在侦听的 IP 地址。如果未设置，则使用默认网络接口。
      </td>
    </tr>

    <tr>
      <td colspan="2">
      <!--
      --apiserver-bind-port int32&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Default: 6443
      -->
      --apiserver-bind-port int32&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;默认值：6443
      </td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      If the node should host a new control plane instance, the port for the API Server to bind to.
      -->
      如果该节点托管一个新的控制平面实例，则为 API 服务器要绑定的端口。
      </td>
    </tr>

    <tr>
      <td colspan="2">--certificate-key string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Use this key to decrypt the certificate secrets uploaded by init.
      -->
      使用此密钥解密由 init 上传的证书 secrets。
      </td>
    </tr>

    <tr>
      <td colspan="2">--config string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Path to kubeadm config file.
      -->
       kubeadm 配置文件的路径。
      </td>
    </tr>

    <tr>
      <td colspan="2">--control-plane</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Create a new control plane instance on this node
      -->
      在此节点上创建一个新的控制平面实例
      </td>
    </tr>

    <tr>
      <td colspan="2">--discovery-file string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      For file-based discovery, a file or URL from which to load cluster information.
      -->
      对于基于文件的发现，给出用于加载集群信息的文件或者 URL。
      </td>
    </tr>

    <tr>
      <td colspan="2">--discovery-token string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      For token-based discovery, the token used to validate cluster information fetched from the API server.
      -->
      对于基于令牌的发现，该令牌用于验证从 API 服务器获取的集群信息。
      </td>
    </tr>

    <tr>
      <td colspan="2">--discovery-token-ca-cert-hash stringSlice</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      For token-based discovery, validate that the root CA public key matches this hash (format: "&lt;type&gt;:&lt;value&gt;").
      -->
      对于基于令牌的发现，请验证根 CA 公钥是否匹配此哈希值（格式："&lt;type&gt;:&lt;value&gt;"）。
      </td>
    </tr>

    <tr>
      <td colspan="2">--discovery-token-unsafe-skip-ca-verification</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      For token-based discovery, allow joining without --discovery-token-ca-cert-hash pinning.
      -->
      对于基于令牌的发现，允许在未关联 --discovery-token-ca-cert-hash 参数的情况下添加节点。
      </td>
    </tr>

    <tr>
      <td colspan="2">-k, --experimental-kustomize string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      The path where kustomize patches for static pod manifests are stored.
      -->
      用于存储 kustomize 为静态 pod 清单所提供的补丁的路径。
      </td>
    </tr>

    <tr>
      <td colspan="2">-h, --help</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      help for all
      -->
       all 操作的帮助命令
      </td>
    </tr>

    <tr>
      <td colspan="2">--node-name string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Specify the node name.
      -->
      指定节点名称。
      </td>
    </tr>

    <tr>
      <td colspan="2">--tls-bootstrap-token string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Specify the token used to temporarily authenticate with the Kubernetes Control Plane while joining the node.
      -->
      指定在加入节点时用于临时通过 Kubernetes 控制平面进行身份验证的令牌。
      </td>
    </tr>

    <tr>
      <td colspan="2">--token string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      Use this token for both discovery-token and tls-bootstrap-token when those values are not provided.
      -->
      如果未提供这些值，则将它们用于 discovery-token 令牌和 tls-bootstrap 令牌。
      </td>
    </tr>

  </tbody>
</table>



<!--
### Options inherited from parent commands
-->
### 从父命令继承的选项

<table style="width: 100%; table-layout: fixed;">
  <colgroup>
    <col span="1" style="width: 10px;" />
    <col span="1" />
  </colgroup>
  <tbody>

    <tr>
      <td colspan="2">--rootfs string</td>
    </tr>
    <tr>
      <td></td><td style="line-height: 130%; word-wrap: break-word;">
      <!--
      [EXPERIMENTAL] The path to the 'real' host root filesystem.
      -->
      [实验] 指向 '真实' 宿主机根文件系统的路径。
      </td>
    </tr>

  </tbody>
</table>



<!--
SEE ALSO
-->
查看其他

<!--
* [kubeadm join phase control-plane-prepare](kubeadm_join_phase_control-plane-prepare.md)	 - Prepare the machine for serving a control plane
-->
* [kubeadm join phase control-plane-prepare](kubeadm_join_phase_control-plane-prepare.md)	 - 准备为控制平面服务的机器

