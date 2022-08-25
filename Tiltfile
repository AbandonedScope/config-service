custom_build(
    ref = 'config-service',
    command = 'gradlew bootBuildImage --imageName %EXPECTED_REF%',
    deps = ['build.gradle', 'src']
)

k8s_yaml(kustomize('k8s'))

k8s_resource('config-service', port_forwards=['8888'])