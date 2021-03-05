---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977806"
---
# <span data-ttu-id="3ceda-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="3ceda-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="3ceda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ceda-102">SYNOPSIS</span></span>
<span data-ttu-id="3ceda-103">Definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3ceda-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="3ceda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ceda-104">SYNTAX</span></span>

### <span data-ttu-id="3ceda-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ceda-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ceda-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ceda-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ceda-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ceda-107">DESCRIPTION</span></span>
<span data-ttu-id="3ceda-108">Il cmdlet **New-AzOperationalInsightsCustomLogDataSource** definisce criteri di raccolta dei log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3ceda-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="3ceda-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ceda-109">EXAMPLES</span></span>

## <span data-ttu-id="3ceda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ceda-110">PARAMETERS</span></span>

### <span data-ttu-id="3ceda-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="3ceda-111">-CustomLogRawJson</span></span>
<span data-ttu-id="3ceda-112">Specifica i criteri di raccolta personalizzati come stringa JSON (JavaScript Object Notation) non elaborata.</span><span class="sxs-lookup"><span data-stu-id="3ceda-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ceda-113">-DefaultProfile</span></span>
<span data-ttu-id="3ceda-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ceda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ceda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3ceda-115">-Force</span></span>
<span data-ttu-id="3ceda-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3ceda-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ceda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3ceda-117">-Name</span></span>
<span data-ttu-id="3ceda-118">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="3ceda-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ceda-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ceda-120">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="3ceda-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3ceda-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3ceda-121">-Workspace</span></span>
<span data-ttu-id="3ceda-122">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ceda-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ceda-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ceda-123">-WorkspaceName</span></span>
<span data-ttu-id="3ceda-124">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ceda-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3ceda-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ceda-125">-Confirm</span></span>
<span data-ttu-id="3ceda-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ceda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ceda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ceda-127">-WhatIf</span></span>
<span data-ttu-id="3ceda-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ceda-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ceda-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ceda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ceda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ceda-130">CommonParameters</span></span>
<span data-ttu-id="3ceda-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ceda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ceda-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ceda-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ceda-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ceda-133">INPUTS</span></span>

### <span data-ttu-id="3ceda-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ceda-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3ceda-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3ceda-135">System.String</span></span>

## <span data-ttu-id="3ceda-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ceda-136">OUTPUTS</span></span>

### <span data-ttu-id="3ceda-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3ceda-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3ceda-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ceda-138">NOTES</span></span>

## <span data-ttu-id="3ceda-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ceda-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ceda-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="3ceda-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="3ceda-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="3ceda-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


