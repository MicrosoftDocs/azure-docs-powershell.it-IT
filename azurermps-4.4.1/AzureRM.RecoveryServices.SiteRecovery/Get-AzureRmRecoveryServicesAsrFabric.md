---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510384"
---
# <span data-ttu-id="827ce-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="827ce-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="827ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="827ce-102">SYNOPSIS</span></span>
<span data-ttu-id="827ce-103">Ottenere i dettagli di un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="827ce-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="827ce-104">SYNTAX</span></span>

### <span data-ttu-id="827ce-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="827ce-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="827ce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="827ce-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="827ce-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="827ce-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="827ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="827ce-108">DESCRIPTION</span></span>
<span data-ttu-id="827ce-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrFabric** ottiene le proprietà di un determinato tessuto di recupero del sito di Azure o di tutti i tessuti di ripristino di Azure site in un caveau di un servizio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="827ce-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="827ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="827ce-110">EXAMPLES</span></span>

### <span data-ttu-id="827ce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="827ce-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="827ce-112">Restituisce tutti i tessuti di ripristino di Azure site nel Vault.</span><span class="sxs-lookup"><span data-stu-id="827ce-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="827ce-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="827ce-113">PARAMETERS</span></span>

### <span data-ttu-id="827ce-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="827ce-114">-FriendlyName</span></span>
<span data-ttu-id="827ce-115">Cercare il tessuto ASR con il nome descrittivo del tessuto.</span><span class="sxs-lookup"><span data-stu-id="827ce-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827ce-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="827ce-116">-Name</span></span>
<span data-ttu-id="827ce-117">Cercare il tessuto ASR in base al nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="827ce-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827ce-118">CommonParameters</span></span>
<span data-ttu-id="827ce-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827ce-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827ce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827ce-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="827ce-121">INPUTS</span></span>

### <span data-ttu-id="827ce-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="827ce-122">None</span></span>

## <span data-ttu-id="827ce-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="827ce-123">OUTPUTS</span></span>

### <span data-ttu-id="827ce-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="827ce-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="827ce-125">Note</span><span class="sxs-lookup"><span data-stu-id="827ce-125">NOTES</span></span>

## <span data-ttu-id="827ce-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="827ce-126">RELATED LINKS</span></span>

[<span data-ttu-id="827ce-127">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="827ce-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="827ce-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="827ce-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
