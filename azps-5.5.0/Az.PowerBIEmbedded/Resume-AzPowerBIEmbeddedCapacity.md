---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189351"
---
# <span data-ttu-id="a655d-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a655d-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a655d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a655d-102">SYNOPSIS</span></span>
<span data-ttu-id="a655d-103">Riprende un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a655d-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="a655d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a655d-104">SYNTAX</span></span>

### <span data-ttu-id="a655d-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a655d-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a655d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a655d-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a655d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a655d-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a655d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a655d-108">DESCRIPTION</span></span>
<span data-ttu-id="a655d-109">Il cmdlet Resume-AzPowerBIEmbeddedCapacity riprendere un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="a655d-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a655d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a655d-110">EXAMPLES</span></span>

### <span data-ttu-id="a655d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a655d-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="a655d-112">Questo comando riprende una capacità sospesa denominata testcapacity nel gruppo di risorse testRG</span><span class="sxs-lookup"><span data-stu-id="a655d-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a655d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a655d-113">PARAMETERS</span></span>

### <span data-ttu-id="a655d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a655d-114">-DefaultProfile</span></span>
<span data-ttu-id="a655d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a655d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a655d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a655d-116">-InputObject</span></span>
<span data-ttu-id="a655d-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="a655d-117">Input object for Piping</span></span>

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

### <span data-ttu-id="a655d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a655d-118">-Name</span></span>
<span data-ttu-id="a655d-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="a655d-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a655d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a655d-120">-PassThru</span></span>
<span data-ttu-id="a655d-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a655d-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a655d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a655d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a655d-123">Nome del gruppo di risorse azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="a655d-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a655d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a655d-124">-ResourceId</span></span>
<span data-ttu-id="a655d-125">ID risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="a655d-125">Azure resource ID</span></span>

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

### <span data-ttu-id="a655d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a655d-126">-Confirm</span></span>
<span data-ttu-id="a655d-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="a655d-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a655d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a655d-128">-WhatIf</span></span>
<span data-ttu-id="a655d-129">Descrive le azioni che l'operazione corrente eseguirà senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="a655d-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a655d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a655d-130">CommonParameters</span></span>
<span data-ttu-id="a655d-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a655d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a655d-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a655d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a655d-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a655d-133">INPUTS</span></span>

### <span data-ttu-id="a655d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a655d-134">System.String</span></span>

### <span data-ttu-id="a655d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a655d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a655d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a655d-136">OUTPUTS</span></span>

### <span data-ttu-id="a655d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a655d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a655d-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="a655d-138">NOTES</span></span>

## <span data-ttu-id="a655d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a655d-139">RELATED LINKS</span></span>

[<span data-ttu-id="a655d-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a655d-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a655d-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a655d-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
