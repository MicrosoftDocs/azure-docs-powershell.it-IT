---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188338"
---
# <span data-ttu-id="b3ea4-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b3ea4-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="b3ea4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ea4-103">Elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-103">Deletes a data source.</span></span>

## <span data-ttu-id="b3ea4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3ea4-104">SYNTAX</span></span>

### <span data-ttu-id="b3ea4-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3ea4-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ea4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b3ea4-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ea4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3ea4-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ea4-108">Il cmdlet **Remove-AzOperationalInsightsDataSource** Elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="b3ea4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3ea4-109">EXAMPLES</span></span>

## <span data-ttu-id="b3ea4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="b3ea4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ea4-111">-DefaultProfile</span></span>
<span data-ttu-id="b3ea4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3ea4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ea4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b3ea4-113">-Force</span></span>
<span data-ttu-id="b3ea4-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3ea4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3ea4-115">-Name</span></span>
<span data-ttu-id="b3ea4-116">Specifica il nome di un'origine dati da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="b3ea4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ea4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3ea4-118">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="b3ea4-119">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b3ea4-119">-Workspace</span></span>
<span data-ttu-id="b3ea4-120">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b3ea4-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3ea4-121">-WorkspaceName</span></span>
<span data-ttu-id="b3ea4-122">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b3ea4-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3ea4-123">-Confirm</span></span>
<span data-ttu-id="b3ea4-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ea4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ea4-125">-WhatIf</span></span>
<span data-ttu-id="b3ea4-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ea4-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ea4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ea4-128">CommonParameters</span></span>
<span data-ttu-id="b3ea4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ea4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ea4-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ea4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ea4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3ea4-131">INPUTS</span></span>

### <span data-ttu-id="b3ea4-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b3ea4-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b3ea4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ea4-133">System.String</span></span>

## <span data-ttu-id="b3ea4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3ea4-134">OUTPUTS</span></span>

### <span data-ttu-id="b3ea4-135">System. void</span><span class="sxs-lookup"><span data-stu-id="b3ea4-135">System.Void</span></span>

## <span data-ttu-id="b3ea4-136">Note</span><span class="sxs-lookup"><span data-stu-id="b3ea4-136">NOTES</span></span>
* <span data-ttu-id="b3ea4-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="b3ea4-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b3ea4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3ea4-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3ea4-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b3ea4-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="b3ea4-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b3ea4-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)

