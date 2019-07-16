# cv_default_org_view_version_export
Patch to export the cv default organization view version

This patch has been tested on-
#tfm-rubygem-hammer_cli_katello-0.16.0.11-1.el7sat.noarch
#satellite-6.5.1-1.el7sat.noarch

Steps to apply the patch-

1- download the cv_import_export_helper.patch

2- Move to the working folder-

#cd /opt/theforeman/tfm/root/usr/share/gems/gems/hammer_cli_katello-0.16.0.11/lib/hammer_cli_katello/

3- Test the patch, below command will not make the changes. It is just to ensure the patch process is error free-

#patch --dry-run < cv_import_export_helper.patch

4- Apply the patch

#patch < cv_import_export_helper.patch

5- Restart the services.

#katello-services restart

6- revert the patch in case of any issues-

#patch -R < cv_import_export_helper.patch

Note: This patch will not persist in subsequent upgrades
