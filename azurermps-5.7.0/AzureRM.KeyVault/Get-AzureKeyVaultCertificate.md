---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512572"
---
# <span data-ttu-id="7274e-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="7274e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7274e-102">SYNOPSIS</span></span>
<span data-ttu-id="7274e-103">Ottiene un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7274e-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7274e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7274e-104">SYNTAX</span></span>

### <span data-ttu-id="7274e-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7274e-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274e-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="7274e-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274e-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="7274e-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274e-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="7274e-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274e-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="7274e-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274e-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="7274e-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7274e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7274e-111">DESCRIPTION</span></span>
<span data-ttu-id="7274e-112">Il cmdlet **Get-AzureKeyVaultCertificate** ottiene il certificato specificato o le versioni di un certificato da un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7274e-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7274e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7274e-113">EXAMPLES</span></span>

### <span data-ttu-id="7274e-114">Esempio 1: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="7274e-114">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="7274e-115">Questo comando ottiene il certificato denominato TestCert01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="7274e-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="7274e-116">Esempio 2: ottenere tutti i certificati eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7274e-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="7274e-117">Questo comando ottiene tutti i certificati eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="7274e-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7274e-118">Esempio 3: Ottiene il certificato Cert che è stato eliminato ma non eliminato per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7274e-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="7274e-119">Questo comando ottiene il certificato denominato "CERT" eliminato in precedenza, ma non eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="7274e-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7274e-120">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata del certificato eliminato.</span><span class="sxs-lookup"><span data-stu-id="7274e-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="7274e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7274e-121">PARAMETERS</span></span>

### <span data-ttu-id="7274e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7274e-122">-DefaultProfile</span></span>
<span data-ttu-id="7274e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7274e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7274e-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7274e-124">-IncludeVersions</span></span>
<span data-ttu-id="7274e-125">Indica che questa operazione ottiene tutte le versioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="7274e-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7274e-126">-InputObject</span></span>
<span data-ttu-id="7274e-127">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="7274e-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7274e-128">-InRemovedState</span></span>
<span data-ttu-id="7274e-129">Specifica se includere i certificati eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="7274e-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="7274e-130">-Name</span></span>
<span data-ttu-id="7274e-131">Specifica il nome del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7274e-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-132">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7274e-132">-VaultName</span></span>
<span data-ttu-id="7274e-133">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7274e-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-134">-Versione</span><span class="sxs-lookup"><span data-stu-id="7274e-134">-Version</span></span>
<span data-ttu-id="7274e-135">Specifica la versione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="7274e-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7274e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7274e-136">CommonParameters</span></span>
<span data-ttu-id="7274e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7274e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7274e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7274e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7274e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7274e-139">INPUTS</span></span>

### <span data-ttu-id="7274e-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7274e-140">None</span></span>
<span data-ttu-id="7274e-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7274e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7274e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7274e-142">OUTPUTS</span></span>

### <span data-ttu-id="7274e-143">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="7274e-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="7274e-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="7274e-145">Note</span><span class="sxs-lookup"><span data-stu-id="7274e-145">NOTES</span></span>

## <span data-ttu-id="7274e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7274e-146">RELATED LINKS</span></span>

[<span data-ttu-id="7274e-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7274e-148">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7274e-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="7274e-150">Undo-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="7274e-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
