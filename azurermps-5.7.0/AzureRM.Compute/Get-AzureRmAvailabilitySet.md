---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516904"
---
# <span data-ttu-id="101e5-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="101e5-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="101e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="101e5-102">SYNOPSIS</span></span>
<span data-ttu-id="101e5-103">Ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="101e5-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="101e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="101e5-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="101e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="101e5-105">DESCRIPTION</span></span>
<span data-ttu-id="101e5-106">Il cmdlet **Get-AzureRmAvailabilitySet** ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="101e5-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="101e5-107">Puoi specificare il nome di un set di disponibilità specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="101e5-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="101e5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="101e5-108">EXAMPLES</span></span>

### <span data-ttu-id="101e5-109">Esempio 1: ottenere un set di disponibilità specifico</span><span class="sxs-lookup"><span data-stu-id="101e5-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="101e5-110">Questo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="101e5-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="101e5-111">Esempio 2: ottenere tutti i set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="101e5-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="101e5-112">Questo comando ottiene tutti i set di disponibilità nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="101e5-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="101e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="101e5-113">PARAMETERS</span></span>

### <span data-ttu-id="101e5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="101e5-114">-Name</span></span>
<span data-ttu-id="101e5-115">Specifica il nome di un set di disponibilità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="101e5-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="101e5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="101e5-116">-ResourceGroupName</span></span>
<span data-ttu-id="101e5-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="101e5-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="101e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101e5-118">CommonParameters</span></span>
<span data-ttu-id="101e5-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="101e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101e5-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101e5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101e5-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="101e5-121">INPUTS</span></span>

### <span data-ttu-id="101e5-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="101e5-122">None</span></span>
<span data-ttu-id="101e5-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="101e5-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="101e5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="101e5-124">OUTPUTS</span></span>

## <span data-ttu-id="101e5-125">Note</span><span class="sxs-lookup"><span data-stu-id="101e5-125">NOTES</span></span>

## <span data-ttu-id="101e5-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="101e5-126">RELATED LINKS</span></span>

[<span data-ttu-id="101e5-127">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="101e5-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="101e5-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="101e5-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


