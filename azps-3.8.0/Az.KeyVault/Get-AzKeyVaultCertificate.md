---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: f4abc9a84f7b9b11bea4e0c7f44d888fc517aaf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018661"
---
# <span data-ttu-id="a4b82-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a4b82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4b82-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b82-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a4b82-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="a4b82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b82-104">SYNTAX</span></span>

### <span data-ttu-id="a4b82-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4b82-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a4b82-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="a4b82-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="a4b82-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="a4b82-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="a4b82-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b82-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b82-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b82-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b82-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b82-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b82-114">DESCRIPTION</span></span>
<span data-ttu-id="a4b82-115">Il cmdlet **Get-AzKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a4b82-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a4b82-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b82-116">EXAMPLES</span></span>

### <span data-ttu-id="a4b82-117">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="a4b82-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="a4b82-118">Esempio 2: ottenere CERT e salvarlo come PFX</span><span class="sxs-lookup"><span data-stu-id="a4b82-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="a4b82-119">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="a4b82-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="a4b82-120">Per scaricare il certificato come file PFX, eseguire il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="a4b82-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="a4b82-121">Questi comandi accedono a SecretId e quindi salvano il contenuto come file PFX.</span><span class="sxs-lookup"><span data-stu-id="a4b82-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.SecretId

$secretByte = [Convert]::FromBase64String($secret.SecretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyValt.pfx", $pfxFileByte)
```

### <span data-ttu-id="a4b82-122">Esempio 3: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a4b82-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="a4b82-123">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a4b82-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a4b82-124">Esempio 4: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a4b82-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="a4b82-125">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a4b82-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a4b82-126">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="a4b82-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="a4b82-127">Esempio 5: elencare i certificati tramite filtro</span><span class="sxs-lookup"><span data-stu-id="a4b82-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="a4b82-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4b82-128">PARAMETERS</span></span>

### <span data-ttu-id="a4b82-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b82-129">-DefaultProfile</span></span>
<span data-ttu-id="a4b82-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4b82-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="a4b82-131">-IncludePending</span></span>
<span data-ttu-id="a4b82-132">Specifica se includere i certificati in sospeso nell'output</span><span class="sxs-lookup"><span data-stu-id="a4b82-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a4b82-133">-IncludeVersions</span></span>
<span data-ttu-id="a4b82-134">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="a4b82-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4b82-135">-InputObject</span></span>
<span data-ttu-id="a4b82-136">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="a4b82-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a4b82-137">-InRemovedState</span></span>
<span data-ttu-id="a4b82-138">Specifica se includere i certificati eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="a4b82-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4b82-139">-Name</span></span>
<span data-ttu-id="a4b82-140">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a4b82-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b82-141">-ResourceId</span></span>
<span data-ttu-id="a4b82-142">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="a4b82-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-143">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a4b82-143">-VaultName</span></span>
<span data-ttu-id="a4b82-144">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a4b82-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-145">-Versione</span><span class="sxs-lookup"><span data-stu-id="a4b82-145">-Version</span></span>
<span data-ttu-id="a4b82-146">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="a4b82-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b82-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b82-147">CommonParameters</span></span>
<span data-ttu-id="a4b82-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b82-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b82-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b82-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b82-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4b82-150">INPUTS</span></span>

### <span data-ttu-id="a4b82-151">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a4b82-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a4b82-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b82-152">System.String</span></span>

## <span data-ttu-id="a4b82-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b82-153">OUTPUTS</span></span>

### <span data-ttu-id="a4b82-154">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a4b82-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="a4b82-155">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="a4b82-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="a4b82-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a4b82-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a4b82-158">Note</span><span class="sxs-lookup"><span data-stu-id="a4b82-158">NOTES</span></span>

## <span data-ttu-id="a4b82-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b82-159">RELATED LINKS</span></span>

[<span data-ttu-id="a4b82-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4b82-161">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4b82-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4b82-163">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="a4b82-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
