---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508099"
---
# <span data-ttu-id="d1247-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1247-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1247-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1247-102">SYNOPSIS</span></span>
<span data-ttu-id="d1247-103">Riprende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d1247-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1247-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1247-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d1247-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1247-105">DESCRIPTION</span></span>
<span data-ttu-id="d1247-106">Il cmdlet Resume-AzureRmPowerBIEmbeddedCapacity riprende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1247-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d1247-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1247-107">EXAMPLES</span></span>

### <span data-ttu-id="d1247-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1247-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="d1247-109">Questo comando riprenderà una capacità sospesa denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="d1247-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="d1247-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1247-110">PARAMETERS</span></span>

### <span data-ttu-id="d1247-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1247-111">-Name</span></span>
<span data-ttu-id="d1247-112">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="d1247-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d1247-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1247-113">-ResourceGroupName</span></span>
<span data-ttu-id="d1247-114">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="d1247-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d1247-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1247-115">-ResourceId</span></span>
<span data-ttu-id="d1247-116">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="d1247-116">Azure resource ID</span></span>

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

### <span data-ttu-id="d1247-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1247-117">-InputObject</span></span>
<span data-ttu-id="d1247-118">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="d1247-118">Input object for Piping</span></span>

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

### <span data-ttu-id="d1247-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1247-119">-Confirm</span></span>
<span data-ttu-id="d1247-120">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="d1247-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d1247-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1247-121">-WhatIf</span></span>
<span data-ttu-id="d1247-122">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="d1247-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d1247-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1247-123">CommonParameters</span></span>
<span data-ttu-id="d1247-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1247-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1247-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1247-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1247-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1247-126">INPUTS</span></span>

### <span data-ttu-id="d1247-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1247-127">None</span></span>
<span data-ttu-id="d1247-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d1247-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1247-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1247-129">OUTPUTS</span></span>

### <span data-ttu-id="d1247-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1247-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1247-131">Note</span><span class="sxs-lookup"><span data-stu-id="d1247-131">NOTES</span></span>

## <span data-ttu-id="d1247-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1247-132">RELATED LINKS</span></span>

[<span data-ttu-id="d1247-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1247-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d1247-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1247-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
