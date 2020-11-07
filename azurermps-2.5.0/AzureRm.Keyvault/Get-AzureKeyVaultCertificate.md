---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866890"
---
# <span data-ttu-id="91b25-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="91b25-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="91b25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91b25-102">SYNOPSIS</span></span>
<span data-ttu-id="91b25-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91b25-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91b25-104">SYNTAX</span></span>

### <span data-ttu-id="91b25-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91b25-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b25-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="91b25-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b25-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="91b25-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b25-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="91b25-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b25-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91b25-109">DESCRIPTION</span></span>
<span data-ttu-id="91b25-110">Il cmdlet **Get-AzureKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="91b25-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="91b25-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91b25-111">EXAMPLES</span></span>

### <span data-ttu-id="91b25-112">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="91b25-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="91b25-113">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="91b25-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="91b25-114">Esempio 2: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91b25-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="91b25-115">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="91b25-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="91b25-116">Esempio 3: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91b25-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="91b25-117">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="91b25-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="91b25-118">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="91b25-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="91b25-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91b25-119">PARAMETERS</span></span>

### <span data-ttu-id="91b25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b25-120">-DefaultProfile</span></span>
<span data-ttu-id="91b25-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="91b25-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b25-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="91b25-122">-IncludeVersions</span></span>
<span data-ttu-id="91b25-123">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="91b25-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="91b25-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="91b25-124">-InRemovedState</span></span>
<span data-ttu-id="91b25-125">Specifica se includere i certificati eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="91b25-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="91b25-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="91b25-126">-Name</span></span>
<span data-ttu-id="91b25-127">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="91b25-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="91b25-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="91b25-128">-VaultName</span></span>
<span data-ttu-id="91b25-129">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91b25-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="91b25-130">-Versione</span><span class="sxs-lookup"><span data-stu-id="91b25-130">-Version</span></span>
<span data-ttu-id="91b25-131">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="91b25-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="91b25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b25-132">CommonParameters</span></span>
<span data-ttu-id="91b25-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b25-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b25-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b25-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91b25-135">INPUTS</span></span>

## <span data-ttu-id="91b25-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91b25-136">OUTPUTS</span></span>

### <span data-ttu-id="91b25-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="91b25-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="91b25-138">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="91b25-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="91b25-139">Note</span><span class="sxs-lookup"><span data-stu-id="91b25-139">NOTES</span></span>

## <span data-ttu-id="91b25-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91b25-140">RELATED LINKS</span></span>

[<span data-ttu-id="91b25-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="91b25-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="91b25-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="91b25-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="91b25-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="91b25-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


