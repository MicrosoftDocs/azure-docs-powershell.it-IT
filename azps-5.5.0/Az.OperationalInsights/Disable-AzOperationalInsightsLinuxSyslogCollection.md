---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179247"
---
# <span data-ttu-id="50607-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="50607-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="50607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50607-102">SYNOPSIS</span></span>
<span data-ttu-id="50607-103">Interrompe la raccolta di dati syslog da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="50607-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="50607-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50607-104">SYNTAX</span></span>

### <span data-ttu-id="50607-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50607-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50607-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50607-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50607-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50607-107">DESCRIPTION</span></span>
<span data-ttu-id="50607-108">Il cmdlet **Disable-AzOperationalInsightsLinuxSyslogCollection** interrompe la raccolta di dati SysLog dai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="50607-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="50607-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50607-109">EXAMPLES</span></span>

## <span data-ttu-id="50607-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50607-110">PARAMETERS</span></span>

### <span data-ttu-id="50607-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50607-111">-DefaultProfile</span></span>
<span data-ttu-id="50607-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="50607-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50607-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50607-113">-ResourceGroupName</span></span>
<span data-ttu-id="50607-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="50607-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="50607-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="50607-115">-Workspace</span></span>
<span data-ttu-id="50607-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50607-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="50607-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50607-117">-WorkspaceName</span></span>
<span data-ttu-id="50607-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50607-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="50607-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50607-119">-Confirm</span></span>
<span data-ttu-id="50607-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50607-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50607-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50607-121">-WhatIf</span></span>
<span data-ttu-id="50607-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50607-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50607-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50607-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50607-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50607-124">CommonParameters</span></span>
<span data-ttu-id="50607-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50607-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50607-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50607-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50607-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="50607-127">INPUTS</span></span>

### <span data-ttu-id="50607-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="50607-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="50607-129">System.String</span><span class="sxs-lookup"><span data-stu-id="50607-129">System.String</span></span>

## <span data-ttu-id="50607-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50607-130">OUTPUTS</span></span>

### <span data-ttu-id="50607-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="50607-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="50607-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="50607-132">NOTES</span></span>
* <span data-ttu-id="50607-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="50607-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="50607-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50607-134">RELATED LINKS</span></span>

[<span data-ttu-id="50607-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="50607-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="50607-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="50607-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


