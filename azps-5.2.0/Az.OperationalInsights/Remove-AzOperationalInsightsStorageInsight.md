---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342031"
---
# <span data-ttu-id="8cf3b-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8cf3b-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="8cf3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cf3b-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf3b-103">Rimuove una panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="8cf3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf3b-104">SYNTAX</span></span>

### <span data-ttu-id="8cf3b-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cf3b-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf3b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8cf3b-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf3b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf3b-107">DESCRIPTION</span></span>
<span data-ttu-id="8cf3b-108">Il cmdlet **Remove-AzOperationalInsightsStorageInsight** Elimina un'analisi dello spazio di archiviazione da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="8cf3b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf3b-109">EXAMPLES</span></span>

### <span data-ttu-id="8cf3b-110">Esempio 1: rimuovere una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="8cf3b-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="8cf3b-111">Questo comando rimuove la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata spazio di lavoro nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="8cf3b-112">Il comando non specifica il parametro *Force* , quindi richiede la conferma prima di rimuovere la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="8cf3b-113">Esempio 2: rimuovere una panoramica dello spazio di archiviazione senza conferma</span><span class="sxs-lookup"><span data-stu-id="8cf3b-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="8cf3b-114">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace. Il secondo comando rimuove la panoramica dello spazio di archiviazione denominata MyStorageInsight da $Workspace senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="8cf3b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cf3b-115">PARAMETERS</span></span>

### <span data-ttu-id="8cf3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf3b-116">-DefaultProfile</span></span>
<span data-ttu-id="8cf3b-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8cf3b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cf3b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8cf3b-118">-Force</span></span>
<span data-ttu-id="8cf3b-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8cf3b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cf3b-120">-Name</span></span>
<span data-ttu-id="8cf3b-121">Specifica il nome dell'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="8cf3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8cf3b-123">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8cf3b-124">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8cf3b-124">-Workspace</span></span>
<span data-ttu-id="8cf3b-125">Specifica l'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="8cf3b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8cf3b-126">-WorkspaceName</span></span>
<span data-ttu-id="8cf3b-127">Specifica il nome dell'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="8cf3b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cf3b-128">-Confirm</span></span>
<span data-ttu-id="8cf3b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf3b-130">-WhatIf</span></span>
<span data-ttu-id="8cf3b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf3b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf3b-133">CommonParameters</span></span>
<span data-ttu-id="8cf3b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf3b-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf3b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf3b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cf3b-136">INPUTS</span></span>

### <span data-ttu-id="8cf3b-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cf3b-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8cf3b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8cf3b-138">System.String</span></span>

## <span data-ttu-id="8cf3b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf3b-139">OUTPUTS</span></span>

### <span data-ttu-id="8cf3b-140">System. void</span><span class="sxs-lookup"><span data-stu-id="8cf3b-140">System.Void</span></span>

## <span data-ttu-id="8cf3b-141">Note</span><span class="sxs-lookup"><span data-stu-id="8cf3b-141">NOTES</span></span>

## <span data-ttu-id="8cf3b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="8cf3b-143">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="8cf3b-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="8cf3b-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cf3b-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


