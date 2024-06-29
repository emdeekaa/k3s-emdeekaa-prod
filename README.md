# k3s-emdeekaa-prod

rm -rf k3s-emdeekaa-prod/
gh repo clone k3s-emdeekaa-prod
cd k3s-emdeekaa-prod/

helm dep update charts/gitea/



kubectl create namespace emdeekaa-gitea

helm install gitea charts/gitea/ --namespace emdeekaa-gitea
