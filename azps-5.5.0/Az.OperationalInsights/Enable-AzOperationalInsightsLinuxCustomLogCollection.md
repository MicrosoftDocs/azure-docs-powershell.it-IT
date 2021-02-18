---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193214"
---
# <span data-ttu-id="e6605-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e6605-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="e6605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6605-102">SYNOPSIS</span></span>
<span data-ttu-id="e6605-103">Avvia la raccolta di log personalizzati da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="e6605-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="e6605-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6605-104">SYNTAX</span></span>

### <span data-ttu-id="e6605-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6605-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6605-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6605-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6605-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6605-107">DESCRIPTION</span></span>
<span data-ttu-id="e6605-108">Il cmdlet **Enable-AzOperationalInsightsLinuxCustomLogCollection avvia** la raccolta di log personalizzati dai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e6605-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e6605-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6605-109">EXAMPLES</span></span>

## <span data-ttu-id="e6605-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6605-110">PARAMETERS</span></span>

### <span data-ttu-id="e6605-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6605-111">-DefaultProfile</span></span>
<span data-ttu-id="e6605-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e6605-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6605-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6605-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6605-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="e6605-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e6605-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e6605-115">-Workspace</span></span>
<span data-ttu-id="e6605-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6605-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e6605-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6605-117">-WorkspaceName</span></span>
<span data-ttu-id="e6605-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6605-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e6605-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6605-119">-Confirm</span></span>
<span data-ttu-id="e6605-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6605-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6605-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6605-121">-WhatIf</span></span>
<span data-ttu-id="e6605-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6605-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6605-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6605-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6605-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6605-124">CommonParameters</span></span>
<span data-ttu-id="e6605-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6605-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6605-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6605-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6605-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6605-127">INPUTS</span></span>

### <span data-ttu-id="e6605-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6605-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e6605-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e6605-129">System.String</span></span>

## <span data-ttu-id="e6605-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6605-130">OUTPUTS</span></span>

### <span data-ttu-id="e6605-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e6605-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e6605-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6605-132">NOTES</span></span>
* <span data-ttu-id="e6605-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="e6605-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e6605-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6605-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6605-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e6605-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


