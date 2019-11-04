```json
{
  "useWhiteList": "boolean",

  "jdbc": {
    "url": "String",
    "username": "String",
    "password": "String"
  },

  "server": {
    "hostName": "String - url e.g. http://127.0.0.1",
    "port": "int",
    "grpcPort": "int",
    "bindingAddress": "String - url with port e.g. http://127.0.0.1:9001",
    "communicationType": "enum REST,GRPC",

    "sslConfig": {
      "tls": "enum STRICT,OFF",
      "generateKeyStoreIfNotExisted": "boolean",
      "serverKeyStore": "Path",
      "serverTlsKeyPath": "Path",
      "serverTlsCertificatePath": "Path",
      "serverKeyStorePassword": "String",
      "serverTrustStore": "Path",
      "serverTrustCertificates": [
        "Path..."
      ],
      "serverTrustStorePassword": "String",
      "serverTrustMode": "Enumeration: CA, TOFU, WHITELIST, CA_OR_TOFU, NONE",
      "clientKeyStore": "Path",
      "clientTlsKeyPath": "Path",
      "clientTlsCertificatePath": "Path",
      "clientKeyStorePassword": "String",
      "clientTrustStore": "Path",
      "clientTrustCertificates": [
        "Path..."
      ],
      "clientTrustStorePassword": "String",
      "clientTrustMode": "Enumeration: CA, TOFU, WHITELIST, CA_OR_TOFU, NONE",
      "knownClientsFile": "Path",
      "knownServersFile": "Path"
    },

    "influxConfig": {
      "hostName": "String - url e.g. http://hostname",
      "port": "int",
      "pushIntervalInSecs": "int",
      "dbName": "String"
    }
  },

  "peer": [
    {
      "url": "String - url e.g. http://127.0.0.1:9000/"
    }
  ],

  "keys": {
    "passwords": [
      "String..."
    ],
    "passwordFile": "Path",
    "azureKeyVaultConfig": {
      "url": "Azure Key Vault url"
    },
    "hashicorpKeyVaultConfig": {
        "url": "Hashicorp Vault url",
        "approlePath": "String (defaults to 'approle' if not set)",
        "tlsKeyStorePath": "Path to jks key store",
        "tlsTrustStorePath": "Path to jks trust store"
    },

    "keyData": [
      {
        "config": {
          "data": {
            "aopts": {
              "variant": "Enum : id,d or i",
              "memory": "int",
              "iterations": "int",
              "parallelism": "int"
            },
            "bytes": "String",
            "snonce": "String",
            "asalt": "String",
            "sbox": "String",
            "password": "String"
          },
          "type": "Enum: argon2sbox or unlocked. If unlocked is defined then config data is required. "
        },
        "privateKey": "String",
        "privateKeyPath": "Path",
        "azureVaultPrivateKeyId": "String",
        "azureVaultPrivateKeyVersion": "String",
        "publicKey": "String",
        "publicKeyPath": "Path",
        "azureVaultPublicKeyId": "String",
        "azureVaultPublicKeyVersion": "String",
        "hashicorpVaultSecretEngineName": "String",
        "hashicorpVaultSecretName": "String",
        "hashicorpVaultSecretVersion": "Integer (defaults to 0 (latest) if not set)",
        "hashicorpVaultPrivateKeyId": "String",
        "hashicorpVaultPublicKeyId": "String"
      }
    ]
  },

  "alwaysSendTo": [
     "String..."
  ],

  "unixSocketFile": "Path"
}
```
