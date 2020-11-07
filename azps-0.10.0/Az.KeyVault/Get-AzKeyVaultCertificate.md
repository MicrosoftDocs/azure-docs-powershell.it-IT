---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861314"
---
# <span data-ttu-id="f8f65-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="f8f65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8f65-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f65-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f8f65-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="f8f65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8f65-104">SYNTAX</span></span>

### <span data-ttu-id="f8f65-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8f65-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f65-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="f8f65-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f65-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="f8f65-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f65-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="f8f65-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f65-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8f65-109">DESCRIPTION</span></span>
<span data-ttu-id="f8f65-110">Il cmdlet **Get-AzKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f8f65-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f8f65-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8f65-111">EXAMPLES</span></span>

### <span data-ttu-id="f8f65-112">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="f8f65-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="f8f65-113">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f8f65-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="f8f65-114">Esempio 2: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f8f65-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="f8f65-115">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="f8f65-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="f8f65-116">Esempio 3: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f8f65-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="f8f65-117">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="f8f65-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="f8f65-118">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="f8f65-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="f8f65-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8f65-119">PARAMETERS</span></span>

### <span data-ttu-id="f8f65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f65-120">-DefaultProfile</span></span>
<span data-ttu-id="f8f65-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f8f65-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8f65-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="f8f65-122">-IncludeVersions</span></span>
<span data-ttu-id="f8f65-123">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="f8f65-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="f8f65-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f8f65-124">-InRemovedState</span></span>
<span data-ttu-id="f8f65-125">Specifica se includere i certificati eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="f8f65-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="f8f65-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8f65-126">-Name</span></span>
<span data-ttu-id="f8f65-127">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f8f65-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="f8f65-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f8f65-128">-VaultName</span></span>
<span data-ttu-id="f8f65-129">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f8f65-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f8f65-130">-Versione</span><span class="sxs-lookup"><span data-stu-id="f8f65-130">-Version</span></span>
<span data-ttu-id="f8f65-131">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="f8f65-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="f8f65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f65-132">CommonParameters</span></span>
<span data-ttu-id="f8f65-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f65-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f65-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f65-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8f65-135">INPUTS</span></span>

### <span data-ttu-id="f8f65-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8f65-136">None</span></span>
<span data-ttu-id="f8f65-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f8f65-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8f65-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8f65-138">OUTPUTS</span></span>

### <span data-ttu-id="f8f65-139">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="f8f65-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="f8f65-140">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="f8f65-141">Note</span><span class="sxs-lookup"><span data-stu-id="f8f65-141">NOTES</span></span>

## <span data-ttu-id="f8f65-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8f65-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8f65-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8f65-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8f65-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="f8f65-146">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="f8f65-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
