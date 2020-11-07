---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686716"
---
# <span data-ttu-id="1e842-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1e842-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1e842-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e842-102">SYNOPSIS</span></span>
<span data-ttu-id="1e842-103">Elimina un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="1e842-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e842-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e842-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="1e842-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e842-105">DESCRIPTION</span></span>
<span data-ttu-id="1e842-106">Il cmdlet Remove-AzureRmPowerBIEmbeddedCapacity Elimina un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="1e842-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1e842-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e842-107">EXAMPLES</span></span>

### <span data-ttu-id="1e842-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e842-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="1e842-109">Questo comando rimuoverà la capacità denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="1e842-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="1e842-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e842-110">PARAMETERS</span></span>

### <span data-ttu-id="1e842-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e842-111">-ResourceGroupName</span></span>
<span data-ttu-id="1e842-112">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="1e842-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="1e842-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e842-113">-Name</span></span>
<span data-ttu-id="1e842-114">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="1e842-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="1e842-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e842-115">-ResourceId</span></span>
<span data-ttu-id="1e842-116">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="1e842-116">Azure resource ID</span></span>

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

### <span data-ttu-id="1e842-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e842-117">-InputObject</span></span>
<span data-ttu-id="1e842-118">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="1e842-118">Input object for Piping</span></span>

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

### <span data-ttu-id="1e842-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e842-119">-PassThru</span></span>
<span data-ttu-id="1e842-120">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="1e842-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e842-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e842-121">-Confirm</span></span>
<span data-ttu-id="1e842-122">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="1e842-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="1e842-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e842-123">-WhatIf</span></span>
<span data-ttu-id="1e842-124">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="1e842-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="1e842-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e842-125">CommonParameters</span></span>
<span data-ttu-id="1e842-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e842-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e842-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e842-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e842-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e842-128">INPUTS</span></span>

### <span data-ttu-id="1e842-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1e842-129">None</span></span>
<span data-ttu-id="1e842-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1e842-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e842-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e842-131">OUTPUTS</span></span>

### <span data-ttu-id="1e842-132">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1e842-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1e842-133">Note</span><span class="sxs-lookup"><span data-stu-id="1e842-133">NOTES</span></span>

## <span data-ttu-id="1e842-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e842-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e842-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1e842-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1e842-136">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1e842-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
