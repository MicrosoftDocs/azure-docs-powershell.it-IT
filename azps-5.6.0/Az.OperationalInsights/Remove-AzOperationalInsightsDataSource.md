---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 1a99f06fac37c0d96a159b0c17afc606d850ee65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989867"
---
# <span data-ttu-id="44cde-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44cde-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="44cde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44cde-102">SYNOPSIS</span></span>
<span data-ttu-id="44cde-103">Elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="44cde-103">Deletes a data source.</span></span>

## <span data-ttu-id="44cde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44cde-104">SYNTAX</span></span>

### <span data-ttu-id="44cde-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44cde-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44cde-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="44cde-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44cde-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44cde-107">DESCRIPTION</span></span>
<span data-ttu-id="44cde-108">Il cmdlet **Remove-AzOperationalInsightsDataSource** elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="44cde-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="44cde-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44cde-109">EXAMPLES</span></span>

## <span data-ttu-id="44cde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44cde-110">PARAMETERS</span></span>

### <span data-ttu-id="44cde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cde-111">-DefaultProfile</span></span>
<span data-ttu-id="44cde-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="44cde-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44cde-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44cde-113">-Force</span></span>
<span data-ttu-id="44cde-114">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="44cde-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44cde-115">-Name</span><span class="sxs-lookup"><span data-stu-id="44cde-115">-Name</span></span>
<span data-ttu-id="44cde-116">Specifica il nome di un'origine dati da eliminare.</span><span class="sxs-lookup"><span data-stu-id="44cde-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="44cde-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cde-117">-ResourceGroupName</span></span>
<span data-ttu-id="44cde-118">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="44cde-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="44cde-119">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="44cde-119">-Workspace</span></span>
<span data-ttu-id="44cde-120">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cde-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="44cde-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44cde-121">-WorkspaceName</span></span>
<span data-ttu-id="44cde-122">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cde-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="44cde-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44cde-123">-Confirm</span></span>
<span data-ttu-id="44cde-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cde-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cde-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cde-125">-WhatIf</span></span>
<span data-ttu-id="44cde-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44cde-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44cde-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44cde-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44cde-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cde-128">CommonParameters</span></span>
<span data-ttu-id="44cde-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cde-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cde-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cde-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cde-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="44cde-131">INPUTS</span></span>

### <span data-ttu-id="44cde-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="44cde-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="44cde-133">System.String</span><span class="sxs-lookup"><span data-stu-id="44cde-133">System.String</span></span>

## <span data-ttu-id="44cde-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44cde-134">OUTPUTS</span></span>

### <span data-ttu-id="44cde-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="44cde-135">System.Void</span></span>

## <span data-ttu-id="44cde-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="44cde-136">NOTES</span></span>
* <span data-ttu-id="44cde-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="44cde-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="44cde-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44cde-138">RELATED LINKS</span></span>

[<span data-ttu-id="44cde-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44cde-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="44cde-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44cde-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


