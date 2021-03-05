---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994488"
---
# <span data-ttu-id="824cf-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="824cf-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="824cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824cf-102">SYNOPSIS</span></span>
<span data-ttu-id="824cf-103">Creare un oggetto in memoria per il gruppo segreto del Vault</span><span class="sxs-lookup"><span data-stu-id="824cf-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="824cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="824cf-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="824cf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="824cf-105">DESCRIPTION</span></span>
<span data-ttu-id="824cf-106">Creare un oggetto in memoria per il gruppo segreto</span><span class="sxs-lookup"><span data-stu-id="824cf-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="824cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="824cf-107">EXAMPLES</span></span>

### <span data-ttu-id="824cf-108">Esempio 1: Creare l'oggetto gruppo segreto del vault</span><span class="sxs-lookup"><span data-stu-id="824cf-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="824cf-109">Questo comando crea l'oggetto gruppo segreto del vault usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="824cf-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="824cf-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="824cf-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="824cf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="824cf-111">PARAMETERS</span></span>

### <span data-ttu-id="824cf-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="824cf-112">-CertificateUrl</span></span>
<span data-ttu-id="824cf-113">URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="824cf-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824cf-114">-Id</span><span class="sxs-lookup"><span data-stu-id="824cf-114">-Id</span></span>
<span data-ttu-id="824cf-115">ID risorsa Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="824cf-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824cf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824cf-116">CommonParameters</span></span>
<span data-ttu-id="824cf-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824cf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824cf-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="824cf-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824cf-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="824cf-119">INPUTS</span></span>

## <span data-ttu-id="824cf-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="824cf-120">OUTPUTS</span></span>

### <span data-ttu-id="824cf-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="824cf-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="824cf-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="824cf-122">NOTES</span></span>

<span data-ttu-id="824cf-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="824cf-123">ALIASES</span></span>

## <span data-ttu-id="824cf-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="824cf-124">RELATED LINKS</span></span>

