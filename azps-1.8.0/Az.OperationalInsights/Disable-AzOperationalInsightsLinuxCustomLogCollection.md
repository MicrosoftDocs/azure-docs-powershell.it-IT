---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f36c6b87ed6e1fc916df228448426a441bc855ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677827"
---
# <span data-ttu-id="829c4-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="829c4-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="829c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="829c4-102">SYNOPSIS</span></span>
<span data-ttu-id="829c4-103">Interrompe la raccolta di registri personalizzati da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="829c4-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="829c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="829c4-104">SYNTAX</span></span>

### <span data-ttu-id="829c4-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="829c4-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="829c4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="829c4-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="829c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="829c4-107">DESCRIPTION</span></span>
<span data-ttu-id="829c4-108">Il cmdlet **Disable-AzOperationalInsightsLinuxCustomLogCollection** interrompe la raccolta di log personalizzati dai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="829c4-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="829c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="829c4-109">EXAMPLES</span></span>

## <span data-ttu-id="829c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="829c4-110">PARAMETERS</span></span>

### <span data-ttu-id="829c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829c4-111">-DefaultProfile</span></span>
<span data-ttu-id="829c4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="829c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="829c4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="829c4-113">-ResourceGroupName</span></span>
<span data-ttu-id="829c4-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="829c4-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="829c4-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="829c4-115">-Workspace</span></span>
<span data-ttu-id="829c4-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="829c4-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="829c4-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="829c4-117">-WorkspaceName</span></span>
<span data-ttu-id="829c4-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="829c4-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="829c4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="829c4-119">-Confirm</span></span>
<span data-ttu-id="829c4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="829c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="829c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829c4-121">-WhatIf</span></span>
<span data-ttu-id="829c4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="829c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829c4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="829c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="829c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829c4-124">CommonParameters</span></span>
<span data-ttu-id="829c4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829c4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829c4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="829c4-127">INPUTS</span></span>

### <span data-ttu-id="829c4-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="829c4-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="829c4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="829c4-129">System.String</span></span>

## <span data-ttu-id="829c4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="829c4-130">OUTPUTS</span></span>

### <span data-ttu-id="829c4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="829c4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="829c4-132">Note</span><span class="sxs-lookup"><span data-stu-id="829c4-132">NOTES</span></span>
* <span data-ttu-id="829c4-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="829c4-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="829c4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="829c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="829c4-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="829c4-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


