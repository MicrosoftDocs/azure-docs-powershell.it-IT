---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 8ec48fe995d6f6be817d418714262706436ebf3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997651"
---
# <span data-ttu-id="39680-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="39680-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="39680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39680-102">SYNOPSIS</span></span>
<span data-ttu-id="39680-103">Interrompe la raccolta dei log di IIS dai computer.</span><span class="sxs-lookup"><span data-stu-id="39680-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="39680-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39680-104">SYNTAX</span></span>

### <span data-ttu-id="39680-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39680-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39680-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="39680-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39680-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39680-107">DESCRIPTION</span></span>
<span data-ttu-id="39680-108">Il cmdlet **Disable-AzOperationalInsightsIISLogCollection** interrompe la raccolta di log di Internet Information Services (IIS) dai computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="39680-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="39680-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39680-109">EXAMPLES</span></span>

## <span data-ttu-id="39680-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39680-110">PARAMETERS</span></span>

### <span data-ttu-id="39680-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39680-111">-DefaultProfile</span></span>
<span data-ttu-id="39680-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="39680-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39680-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39680-113">-ResourceGroupName</span></span>
<span data-ttu-id="39680-114">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="39680-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39680-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="39680-115">-Workspace</span></span>
<span data-ttu-id="39680-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39680-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39680-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39680-117">-WorkspaceName</span></span>
<span data-ttu-id="39680-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39680-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39680-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39680-119">-Confirm</span></span>
<span data-ttu-id="39680-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39680-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39680-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39680-121">-WhatIf</span></span>
<span data-ttu-id="39680-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39680-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39680-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39680-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39680-124">CommonParameters</span></span>
<span data-ttu-id="39680-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39680-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39680-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39680-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="39680-127">INPUTS</span></span>

### <span data-ttu-id="39680-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="39680-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="39680-129">System.String</span><span class="sxs-lookup"><span data-stu-id="39680-129">System.String</span></span>

## <span data-ttu-id="39680-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39680-130">OUTPUTS</span></span>

### <span data-ttu-id="39680-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="39680-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="39680-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="39680-132">NOTES</span></span>
* <span data-ttu-id="39680-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="39680-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="39680-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39680-134">RELATED LINKS</span></span>

[<span data-ttu-id="39680-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="39680-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


