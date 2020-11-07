---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 67858083ed648e2965ea6fad2900ab63ef453901
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677823"
---
# <span data-ttu-id="d936f-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d936f-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="d936f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d936f-102">SYNOPSIS</span></span>
<span data-ttu-id="d936f-103">Avvia la raccolta di registri personalizzati da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="d936f-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="d936f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d936f-104">SYNTAX</span></span>

### <span data-ttu-id="d936f-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d936f-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d936f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d936f-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d936f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d936f-107">DESCRIPTION</span></span>
<span data-ttu-id="d936f-108">Il cmdlet **Enable-AzOperationalInsightsLinuxCustomLogCollection** avvia la raccolta di registri personalizzati da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d936f-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d936f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d936f-109">EXAMPLES</span></span>

## <span data-ttu-id="d936f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d936f-110">PARAMETERS</span></span>

### <span data-ttu-id="d936f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d936f-111">-DefaultProfile</span></span>
<span data-ttu-id="d936f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d936f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d936f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d936f-113">-ResourceGroupName</span></span>
<span data-ttu-id="d936f-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="d936f-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d936f-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d936f-115">-Workspace</span></span>
<span data-ttu-id="d936f-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d936f-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d936f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d936f-117">-WorkspaceName</span></span>
<span data-ttu-id="d936f-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d936f-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d936f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d936f-119">-Confirm</span></span>
<span data-ttu-id="d936f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d936f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d936f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d936f-121">-WhatIf</span></span>
<span data-ttu-id="d936f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d936f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d936f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d936f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d936f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d936f-124">CommonParameters</span></span>
<span data-ttu-id="d936f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d936f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d936f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d936f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d936f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d936f-127">INPUTS</span></span>

### <span data-ttu-id="d936f-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d936f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d936f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d936f-129">System.String</span></span>

## <span data-ttu-id="d936f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d936f-130">OUTPUTS</span></span>

### <span data-ttu-id="d936f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d936f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d936f-132">Note</span><span class="sxs-lookup"><span data-stu-id="d936f-132">NOTES</span></span>
* <span data-ttu-id="d936f-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="d936f-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d936f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d936f-134">RELATED LINKS</span></span>

[<span data-ttu-id="d936f-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d936f-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


