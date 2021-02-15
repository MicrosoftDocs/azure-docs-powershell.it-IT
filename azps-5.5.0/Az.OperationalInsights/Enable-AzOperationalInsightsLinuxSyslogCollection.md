---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189430"
---
# <span data-ttu-id="d0600-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d0600-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="d0600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0600-102">SYNOPSIS</span></span>
<span data-ttu-id="d0600-103">Avvia la raccolta di dati SysLog da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="d0600-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="d0600-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0600-104">SYNTAX</span></span>

### <span data-ttu-id="d0600-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0600-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0600-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0600-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0600-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0600-107">DESCRIPTION</span></span>
<span data-ttu-id="d0600-108">Il cmdlet **Enable-AzOperationalInsightsLinuxSyslogCollection avvia** la raccolta di dati SysLog dai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d0600-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d0600-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0600-109">EXAMPLES</span></span>

## <span data-ttu-id="d0600-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0600-110">PARAMETERS</span></span>

### <span data-ttu-id="d0600-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0600-111">-DefaultProfile</span></span>
<span data-ttu-id="d0600-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d0600-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0600-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0600-113">-ResourceGroupName</span></span>
<span data-ttu-id="d0600-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="d0600-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d0600-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d0600-115">-Workspace</span></span>
<span data-ttu-id="d0600-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0600-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0600-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0600-117">-WorkspaceName</span></span>
<span data-ttu-id="d0600-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0600-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0600-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0600-119">-Confirm</span></span>
<span data-ttu-id="d0600-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0600-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0600-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0600-121">-WhatIf</span></span>
<span data-ttu-id="d0600-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0600-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0600-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0600-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0600-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0600-124">CommonParameters</span></span>
<span data-ttu-id="d0600-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0600-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0600-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0600-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0600-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0600-127">INPUTS</span></span>

### <span data-ttu-id="d0600-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0600-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d0600-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d0600-129">System.String</span></span>

## <span data-ttu-id="d0600-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0600-130">OUTPUTS</span></span>

### <span data-ttu-id="d0600-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d0600-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d0600-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0600-132">NOTES</span></span>
* <span data-ttu-id="d0600-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="d0600-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d0600-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0600-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0600-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d0600-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="d0600-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="d0600-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


