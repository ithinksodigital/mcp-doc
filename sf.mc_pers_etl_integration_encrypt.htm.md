

# Encrypt Sensitive Data

Use the Personalization public PGP key to encrypt sensitive data in your ETL
data feeds. Because Personalization uses a secure file transfer protocol
(SFTP) to process ETL data feeds, you don’t need to use PGP encryption unless
your organization requires it.

## How Personalization Handles Encrypted Files

Personalization holds the decryption key and decrypts ETL files only during
reading and processing. The ETL files themselves remain encrypted.

## Personalization PGP Public Key

To encrypt your ETL data before uploading it, enter the Personalization PGP
public key into your PGP application according to its procedures. There’s
nothing to configure in Personalization, but it’s best practice to test the
process by manually uploading an ETL file without committing the changes.
Running a successful test file ensures that the data encryption performs as
expected.

Enter the following into your PGP application:

    
    
    -----BEGIN PGP PUBLIC KEY BLOCK-----
    
    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
    2k560UYBIlaB9w==
    =muvY
    -----END PGP PUBLIC KEY BLOCK-----
    

