---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398819"
---
# <span data-ttu-id="6d5ac-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5ac-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="6d5ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5ac-103">Recupera un certificato da un vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="6d5ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d5ac-104">SYNTAX</span></span>

### <span data-ttu-id="6d5ac-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d5ac-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d5ac-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="6d5ac-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5ac-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="6d5ac-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5ac-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="6d5ac-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5ac-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d5ac-109">DESCRIPTION</span></span>
<span data-ttu-id="6d5ac-110">Il cmdlet **Get-AzKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un vault delle chiavi nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6d5ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d5ac-111">EXAMPLES</span></span>

### <span data-ttu-id="6d5ac-112">Esempio 1: Ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="6d5ac-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="6d5ac-113">Questo comando recupera il certificato denominato TestCert01 dalla chiave vault denominata ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="6d5ac-114">Esempio 2: Ottenere tutti i certificati che sono stati eliminati ma non eliminati per il vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="6d5ac-115">Questo comando recupera tutti i certificati che sono stati eliminati in precedenza, ma non eliminati, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="6d5ac-116">Esempio 3: recupera il certificato MyCert eliminato ma non ripulito per questo vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="6d5ac-117">Questo comando recupera il certificato denominato "MyCert" eliminato in precedenza, ma non ripulito, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="6d5ac-118">Questo comando restituisce metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="6d5ac-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5ac-119">PARAMETERS</span></span>

### <span data-ttu-id="6d5ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5ac-120">-DefaultProfile</span></span>
<span data-ttu-id="6d5ac-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d5ac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="6d5ac-122">-IncludeVersions</span></span>
<span data-ttu-id="6d5ac-123">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6d5ac-124">-InRemovedState</span></span>
<span data-ttu-id="6d5ac-125">Specifica se includere nell'output certificati eliminati in precedenza</span><span class="sxs-lookup"><span data-stu-id="6d5ac-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5ac-126">-Name</span></span>
<span data-ttu-id="6d5ac-127">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6d5ac-128">-VaultName</span></span>
<span data-ttu-id="6d5ac-129">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-129">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-130">-Version</span><span class="sxs-lookup"><span data-stu-id="6d5ac-130">-Version</span></span>
<span data-ttu-id="6d5ac-131">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5ac-132">CommonParameters</span></span>
<span data-ttu-id="6d5ac-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5ac-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5ac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5ac-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d5ac-135">INPUTS</span></span>

### <span data-ttu-id="6d5ac-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6d5ac-136">None</span></span>
<span data-ttu-id="6d5ac-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6d5ac-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d5ac-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d5ac-138">OUTPUTS</span></span>

### <span data-ttu-id="6d5ac-139">System.Collections.generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="6d5ac-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="6d5ac-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5ac-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="6d5ac-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d5ac-141">NOTES</span></span>

## <span data-ttu-id="6d5ac-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d5ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d5ac-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5ac-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="6d5ac-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5ac-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="6d5ac-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5ac-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

