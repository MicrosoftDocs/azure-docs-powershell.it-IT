---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 351a24f2307a09422df4c923b3088f6a39661fd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677821"
---
# <span data-ttu-id="68295-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="68295-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="68295-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68295-102">SYNOPSIS</span></span>
<span data-ttu-id="68295-103">Avvia la raccolta di dati syslog da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="68295-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="68295-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68295-104">SYNTAX</span></span>

### <span data-ttu-id="68295-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68295-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68295-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="68295-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68295-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68295-107">DESCRIPTION</span></span>
<span data-ttu-id="68295-108">Il cmdlet **Enable-AzOperationalInsightsLinuxSyslogCollection** avvia la raccolta di dati syslog da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="68295-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="68295-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68295-109">EXAMPLES</span></span>

## <span data-ttu-id="68295-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68295-110">PARAMETERS</span></span>

### <span data-ttu-id="68295-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68295-111">-DefaultProfile</span></span>
<span data-ttu-id="68295-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68295-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68295-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68295-113">-ResourceGroupName</span></span>
<span data-ttu-id="68295-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="68295-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="68295-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="68295-115">-Workspace</span></span>
<span data-ttu-id="68295-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68295-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="68295-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68295-117">-WorkspaceName</span></span>
<span data-ttu-id="68295-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68295-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="68295-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68295-119">-Confirm</span></span>
<span data-ttu-id="68295-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68295-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68295-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68295-121">-WhatIf</span></span>
<span data-ttu-id="68295-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68295-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68295-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68295-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68295-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68295-124">CommonParameters</span></span>
<span data-ttu-id="68295-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68295-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68295-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68295-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68295-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68295-127">INPUTS</span></span>

### <span data-ttu-id="68295-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="68295-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="68295-129">System. String</span><span class="sxs-lookup"><span data-stu-id="68295-129">System.String</span></span>

## <span data-ttu-id="68295-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68295-130">OUTPUTS</span></span>

### <span data-ttu-id="68295-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="68295-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="68295-132">Note</span><span class="sxs-lookup"><span data-stu-id="68295-132">NOTES</span></span>
* <span data-ttu-id="68295-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="68295-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="68295-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68295-134">RELATED LINKS</span></span>

[<span data-ttu-id="68295-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="68295-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="68295-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="68295-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

