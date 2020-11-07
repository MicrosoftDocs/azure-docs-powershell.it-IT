---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 5935706c341fac5f0b26d3e4965f226342c3dfc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835772"
---
# <span data-ttu-id="98b64-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="98b64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98b64-102">SYNOPSIS</span></span>
<span data-ttu-id="98b64-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="98b64-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="98b64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98b64-104">SYNTAX</span></span>

### <span data-ttu-id="98b64-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98b64-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="98b64-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="98b64-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="98b64-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="98b64-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="98b64-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="98b64-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="98b64-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b64-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="98b64-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98b64-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98b64-114">DESCRIPTION</span></span>
<span data-ttu-id="98b64-115">Il cmdlet **Get-AzKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="98b64-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="98b64-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98b64-116">EXAMPLES</span></span>

### <span data-ttu-id="98b64-117">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="98b64-117">Example 1: Get a certificate</span></span>
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

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="98b64-118">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="98b64-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="98b64-119">Esempio 2: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="98b64-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="98b64-120">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="98b64-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="98b64-121">Esempio 3: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="98b64-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="98b64-122">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="98b64-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="98b64-123">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="98b64-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="98b64-124">Esempio 4: elencare i certificati tramite filtro</span><span class="sxs-lookup"><span data-stu-id="98b64-124">Example 4: List certificates using filtering</span></span>
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

## <span data-ttu-id="98b64-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98b64-125">PARAMETERS</span></span>

### <span data-ttu-id="98b64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b64-126">-DefaultProfile</span></span>
<span data-ttu-id="98b64-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98b64-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98b64-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="98b64-128">-IncludePending</span></span>
<span data-ttu-id="98b64-129">Specifica se includere i certificati in sospeso nell'output</span><span class="sxs-lookup"><span data-stu-id="98b64-129">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="98b64-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="98b64-130">-IncludeVersions</span></span>
<span data-ttu-id="98b64-131">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="98b64-131">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="98b64-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b64-132">-InputObject</span></span>
<span data-ttu-id="98b64-133">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="98b64-133">KeyVault object.</span></span>

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

### <span data-ttu-id="98b64-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98b64-134">-InRemovedState</span></span>
<span data-ttu-id="98b64-135">Specifica se includere i certificati eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="98b64-135">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="98b64-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="98b64-136">-Name</span></span>
<span data-ttu-id="98b64-137">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="98b64-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="98b64-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98b64-138">-ResourceId</span></span>
<span data-ttu-id="98b64-139">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="98b64-139">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="98b64-140">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="98b64-140">-VaultName</span></span>
<span data-ttu-id="98b64-141">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="98b64-141">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="98b64-142">-Versione</span><span class="sxs-lookup"><span data-stu-id="98b64-142">-Version</span></span>
<span data-ttu-id="98b64-143">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="98b64-143">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="98b64-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b64-144">CommonParameters</span></span>
<span data-ttu-id="98b64-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b64-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b64-146">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98b64-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b64-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98b64-147">INPUTS</span></span>

### <span data-ttu-id="98b64-148">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="98b64-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="98b64-149">System. String</span><span class="sxs-lookup"><span data-stu-id="98b64-149">System.String</span></span>

## <span data-ttu-id="98b64-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98b64-150">OUTPUTS</span></span>

### <span data-ttu-id="98b64-151">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98b64-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="98b64-152">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="98b64-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="98b64-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98b64-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="98b64-155">Note</span><span class="sxs-lookup"><span data-stu-id="98b64-155">NOTES</span></span>

## <span data-ttu-id="98b64-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98b64-156">RELATED LINKS</span></span>

[<span data-ttu-id="98b64-157">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="98b64-158">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="98b64-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="98b64-160">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="98b64-160">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
