---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688630"
---
# <span data-ttu-id="af96c-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="af96c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af96c-102">SYNOPSIS</span></span>
<span data-ttu-id="af96c-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="af96c-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af96c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af96c-104">SYNTAX</span></span>

### <span data-ttu-id="af96c-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af96c-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af96c-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="af96c-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af96c-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="af96c-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af96c-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="af96c-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af96c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af96c-109">DESCRIPTION</span></span>
<span data-ttu-id="af96c-110">Il cmdlet **Get-AzureKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="af96c-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="af96c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af96c-111">EXAMPLES</span></span>

### <span data-ttu-id="af96c-112">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="af96c-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="af96c-113">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="af96c-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="af96c-114">Esempio 2: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="af96c-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="af96c-115">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="af96c-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="af96c-116">Esempio 3: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="af96c-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="af96c-117">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="af96c-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="af96c-118">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="af96c-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="af96c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af96c-119">PARAMETERS</span></span>

### <span data-ttu-id="af96c-120">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="af96c-120">-IncludeVersions</span></span>
<span data-ttu-id="af96c-121">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="af96c-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-122">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="af96c-122">-InRemovedState</span></span>
<span data-ttu-id="af96c-123">Specifica se includere i certificati eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="af96c-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="af96c-124">-Name</span></span>
<span data-ttu-id="af96c-125">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="af96c-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-126">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="af96c-126">-VaultName</span></span>
<span data-ttu-id="af96c-127">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="af96c-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-128">-Versione</span><span class="sxs-lookup"><span data-stu-id="af96c-128">-Version</span></span>
<span data-ttu-id="af96c-129">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="af96c-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af96c-130">-DefaultProfile</span></span>
<span data-ttu-id="af96c-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af96c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af96c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af96c-132">CommonParameters</span></span>
<span data-ttu-id="af96c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af96c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af96c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af96c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af96c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af96c-135">INPUTS</span></span>

## <span data-ttu-id="af96c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af96c-136">OUTPUTS</span></span>

### <span data-ttu-id="af96c-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="af96c-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="af96c-138">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="af96c-139">Note</span><span class="sxs-lookup"><span data-stu-id="af96c-139">NOTES</span></span>

## <span data-ttu-id="af96c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af96c-140">RELATED LINKS</span></span>

[<span data-ttu-id="af96c-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="af96c-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="af96c-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="af96c-144">Undo-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="af96c-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
