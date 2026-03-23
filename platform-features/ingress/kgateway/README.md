# Wrapper Chart: kgateway + default Gateway + NodePort-Service
# Führe vor dem ersten Install aus: helm dependency update

helm upgrade --install -n kgateway-system kgateway . \
  -f values.yaml

# kind-cluster: extraPortMappings für NodePort-Zugriff vom Host (z.B. in kind-config):
#   extraPortMappings:
#     - containerPort: 30080
#       hostPort: 30080
#       protocol: TCP
#     - containerPort: 30443
#       hostPort: 30443
#       protocol: TCP
