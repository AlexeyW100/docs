To configure the SDK, create configuration files in your home folder and set the following in them:

- The static key in the file `.aws/credentials`:

   ```
   [default]
               aws_access_key_id = <id>
               aws_secret_access_key = <secretKey>
   ```

- The default region in the file `.aws/config`:

   ```
   [default]
               region=RU-CENTRAL
   ```

   > [!NOTE]
   >
   > To work with Yandex Object Storage, always specify the `RU-CENTRAL` region. A different value of the region may lead to an authorization error.

