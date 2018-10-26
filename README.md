Generate Sign Cert
=========

Generate ssl certificate and sign with existing CA

This role assumes you have already securely placed your ca files locally.

Role Variables
--------------

Sets cert expire time:
cert_expiry: 87600h

Set cert size, e.g. 2048, 4096, etc
cert_size: 2048

Algorithm to use:
cert_algo: rsa

Common name, (comma seperate multiple CNs):
cert_cn: example.com

Where to output generated certificate, key and CSR
cert_output_dir: /tmp/generated_certs

Include CA certificate in output directory:
cert_include_ca_cert: true

Prefix name of output files:
cert_prefix: cert

Where to find the CAs:
ca_dir: /tmp/ca_files

Filename of the CA certificate:
ca_cert_file: ca.pem

Filename of the CA key:
ca_key_file: ca-key.pem

Remove CA source after generate:
ca_remove_after_generate: true

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - entanet_devops.generate_sign_cert

License
-------

BSD