---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865954"
---
# <span data-ttu-id="d2702-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d2702-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d2702-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2702-102">SYNOPSIS</span></span>
<span data-ttu-id="d2702-103">Ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2702-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2702-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2702-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2702-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2702-105">DESCRIPTION</span></span>
<span data-ttu-id="d2702-106">Il cmdlet **Get-AzureRmAvailabilitySet** ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2702-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d2702-107">Puoi specificare il nome di un set di disponibilità specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d2702-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d2702-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2702-108">EXAMPLES</span></span>

### <span data-ttu-id="d2702-109">Esempio 1: ottenere un set di disponibilità specifico</span><span class="sxs-lookup"><span data-stu-id="d2702-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="d2702-110">Questo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d2702-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d2702-111">Esempio 2: ottenere tutti i set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="d2702-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d2702-112">Questo comando ottiene tutti i set di disponibilità nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d2702-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d2702-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2702-113">PARAMETERS</span></span>

### <span data-ttu-id="d2702-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2702-114">-DefaultProfile</span></span>
<span data-ttu-id="d2702-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2702-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2702-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2702-116">-Name</span></span>
<span data-ttu-id="d2702-117">Specifica il nome di un set di disponibilità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2702-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d2702-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2702-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2702-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2702-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2702-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2702-120">CommonParameters</span></span>
<span data-ttu-id="d2702-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2702-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2702-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2702-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2702-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2702-123">INPUTS</span></span>

### <span data-ttu-id="d2702-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2702-124">None</span></span>
<span data-ttu-id="d2702-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d2702-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2702-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2702-126">OUTPUTS</span></span>

### <span data-ttu-id="d2702-127">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d2702-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d2702-128">Note</span><span class="sxs-lookup"><span data-stu-id="d2702-128">NOTES</span></span>

## <span data-ttu-id="d2702-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2702-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2702-130">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d2702-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d2702-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d2702-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


