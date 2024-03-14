Kubectl deployment:

cd kubectl

namespace==>nycb:
kubectl apply -f gui.yml -n nycb
kubectl apply -f stp.yml -n nycb
kubectl apply -f gateway.yml -n nycb
-----------------------------------------------
namespace==>tcb:
kubectl apply -f gui.yml -n tcb
kubectl apply -f stp.yml -n tcb
kubectl apply -f gateway.yml -n tcb

---------------------------------------------------------------

Helm chart deployment:

cd helm-chart
helm create gui
helm create stp
helm create gateway 
----------------------------------------------------------------
namespace==>nycb:
helm install nycb-gui gui/ --namespace nycb
helm install nycb-stp stp/ --namespace nycb
helm install nycb-gateway gateway/ --namespace nycb
----------------------------------------------------------------
namespace==>tcb:
helm install tcb-gui gui/ --namespace tcb
helm install tcb-stp stp/ --namespace tcb
helm install tcb-gateway gateway/ --namespace tcb

----------------------------------------------------------------
