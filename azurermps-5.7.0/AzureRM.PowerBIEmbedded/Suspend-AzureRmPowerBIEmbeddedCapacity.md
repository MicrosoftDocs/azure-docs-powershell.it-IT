---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508084"
---
# <span data-ttu-id="491f9-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="491f9-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="491f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="491f9-102">SYNOPSIS</span></span>
<span data-ttu-id="491f9-103">Sospende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="491f9-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="491f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="491f9-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="491f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="491f9-105">DESCRIPTION</span></span>
<span data-ttu-id="491f9-106">Il cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity sospende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="491f9-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="491f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="491f9-107">EXAMPLES</span></span>

### <span data-ttu-id="491f9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="491f9-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="491f9-109">Questo comando sospenderà una capacità attiva denominata testcapacity nel ResourceGroup TestGroup</span><span class="sxs-lookup"><span data-stu-id="491f9-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="491f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="491f9-110">PARAMETERS</span></span>

### <span data-ttu-id="491f9-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="491f9-111">-Name</span></span>
<span data-ttu-id="491f9-112">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="491f9-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="491f9-113">-ResourceGroupName</span></span>
<span data-ttu-id="491f9-114">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="491f9-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="491f9-115">-ResourceId</span></span>
<span data-ttu-id="491f9-116">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="491f9-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="491f9-117">-InputObject</span></span>
<span data-ttu-id="491f9-118">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="491f9-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="491f9-119">-Confirm</span></span>
<span data-ttu-id="491f9-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="491f9-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491f9-121">-WhatIf</span></span>
<span data-ttu-id="491f9-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="491f9-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491f9-123">CommonParameters</span></span>
<span data-ttu-id="491f9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491f9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491f9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="491f9-126">INPUTS</span></span>

### <span data-ttu-id="491f9-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="491f9-127">None</span></span>
<span data-ttu-id="491f9-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="491f9-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="491f9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="491f9-129">OUTPUTS</span></span>

### <span data-ttu-id="491f9-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="491f9-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="491f9-131">Note</span><span class="sxs-lookup"><span data-stu-id="491f9-131">NOTES</span></span>

## <span data-ttu-id="491f9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="491f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="491f9-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="491f9-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="491f9-134">Curriculum vitae-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="491f9-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

