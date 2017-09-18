# Images

Packer configs.

Requires installation of the [vsphere plugin](https://github.com/jetbrains-infra/packer-builder-vsphere/releases). Download the appropriate plugin and put it in $HOME/.packer.d/plugins

# Usage

This job is configured to trigger the build of another job by the name of "tomcat". The tomcat packer config is almost exactly the same, but the source template of the tomcat job is the same as the destination template of this base job. That means the tomcat build inherits the artifact produced by this build.

Any configuration should be done in the "playbook.yml" ansible playbook. This allows us to keep our packer and jenkins configs clean and dedicated to their tasks.
