# Authorization in Yandex.Cloud

When a user does something with a resource in Yandex.Cloud, IAM checks whether the user has the necessary access rights to perform this operation.

Users get permissions along with resource roles. For more information about how roles are assigned and how the list of permissions is checked, see [[!TITLE]](../access-control/index.md).

## Authentication in Yandex.Cloud

Before authorization, a user must get authenticated, i.e., log in under their account. Authentication is performed in different ways, depending on the type of account and the interface used.

### Authentication with a Yandex.Passport account {#passport}

---

**[!TAB Management console]**

Authentication is carried out automatically when you log in to your Yandex or Yandex.Connect account.

**[!TAB CLI]**

To configure authentication in the CLI, enter your [OAuth token](oauth-token.md) during [profile initialization](../../../cli/quickstart.md#initialize). The token will be saved in the profile configuration and authentication will work automatically.

**[!TAB API]**

[!INCLUDE [owner-warning](../../../_includes/iam/owner-warning.md)]

To perform operations in the API:

1. [Get an IAM token](../../operations/iam-token/create.md) in exchange for your [OAuth token](oauth-token.md).

2. [!INCLUDE [iam-token-usage](../../../_includes/iam-token-usage.md)]

    [!INCLUDE [iam-token-lifetime](../../../_includes/iam-token-lifetime.md)]

---

### Service account authentication {#sa}

---

**[!TAB CLI]**

To perform operations on behalf of your service account, specify the path to its authorized key in the `service-account-key` configuration during [profile initialization](../../../cli/quickstart.md#initialize). The key will be saved in the profile configuration and authentication will work automatically.

**[!TAB API]**

There are three ways to perform operations on behalf of a service account:

* Using an [IAM token](iam-token.md). This is the recommended authentication method. However, please note that the IAM token validity is limited. Therefore, this method is suitable for developing applications that will request the IAM token automatically.

    [Instructions for how to get an IAM token](../../operations/iam-token/create-for-sa.md).

* Using [API keys](api-key).

    [!INCLUDE [api-keys-disclaimer](../../../_includes/iam/api-keys-disclaimer.md)]

    [Instructions for how to get an API key](../../operations/api-key/create.md).

* Using [static access keys](access-key.md). This method should be used in services with an AWS-compatible API, such as [!KEYREF objstorage-name] and [!KEYREF message-queue-name].

    [Instructions for how to get a static access key](../../operations/sa/create-access-key.md).

---

