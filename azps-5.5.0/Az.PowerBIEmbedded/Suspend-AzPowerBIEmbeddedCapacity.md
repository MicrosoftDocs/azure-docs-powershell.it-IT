---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183943"
---
# <span data-ttu-id="afaae-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="afaae-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="afaae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afaae-102">SYNOPSIS</span></span>
<span data-ttu-id="afaae-103">Sospende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="afaae-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="afaae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afaae-104">SYNTAX</span></span>

### <span data-ttu-id="afaae-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afaae-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afaae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="afaae-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afaae-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="afaae-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afaae-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="afaae-108">DESCRIPTION</span></span>
<span data-ttu-id="afaae-109">Il cmdlet Suspend-AzPowerBIEmbeddedCapacity sospende un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="afaae-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="afaae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afaae-110">EXAMPLES</span></span>

### <span data-ttu-id="afaae-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afaae-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="afaae-112">Questo comando sospende una capacità attiva denominata testcapacity nel gruppo di test del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="afaae-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="afaae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afaae-113">PARAMETERS</span></span>

### <span data-ttu-id="afaae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaae-114">-DefaultProfile</span></span>
<span data-ttu-id="afaae-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afaae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afaae-116">-InputObject</span></span>
<span data-ttu-id="afaae-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="afaae-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="afaae-118">-Name</span></span>
<span data-ttu-id="afaae-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="afaae-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afaae-120">-PassThru</span></span>
<span data-ttu-id="afaae-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="afaae-121">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afaae-122">-ResourceGroupName</span></span>
<span data-ttu-id="afaae-123">Nome del gruppo di risorse azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="afaae-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afaae-124">-ResourceId</span></span>
<span data-ttu-id="afaae-125">ID risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="afaae-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afaae-126">-Confirm</span></span>
<span data-ttu-id="afaae-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="afaae-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afaae-128">-WhatIf</span></span>
<span data-ttu-id="afaae-129">Descrive le azioni che l'operazione corrente eseguirà senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="afaae-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaae-130">CommonParameters</span></span>
<span data-ttu-id="afaae-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaae-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afaae-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaae-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="afaae-133">INPUTS</span></span>

### <span data-ttu-id="afaae-134">System.String</span><span class="sxs-lookup"><span data-stu-id="afaae-134">System.String</span></span>

### <span data-ttu-id="afaae-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="afaae-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="afaae-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afaae-136">OUTPUTS</span></span>

### <span data-ttu-id="afaae-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="afaae-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="afaae-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="afaae-138">NOTES</span></span>

## <span data-ttu-id="afaae-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afaae-139">RELATED LINKS</span></span>

[<span data-ttu-id="afaae-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="afaae-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="afaae-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="afaae-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

