---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cbbbd23a42f2922273811a7925cbae6f6fd867f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513103"
---
# <span data-ttu-id="99971-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="99971-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="99971-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99971-102">SYNOPSIS</span></span>
<span data-ttu-id="99971-103">Rimuove una panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99971-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99971-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99971-104">SYNTAX</span></span>

### <span data-ttu-id="99971-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99971-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99971-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="99971-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99971-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99971-107">DESCRIPTION</span></span>
<span data-ttu-id="99971-108">Il cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** Elimina un'analisi dello spazio di archiviazione da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="99971-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="99971-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99971-109">EXAMPLES</span></span>

### <span data-ttu-id="99971-110">Esempio 1: rimuovere una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="99971-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="99971-111">Questo comando rimuove la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata spazio di lavoro nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="99971-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="99971-112">Il comando non specifica il parametro *Force* , quindi richiede la conferma prima di rimuovere la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99971-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="99971-113">Esempio 2: rimuovere una panoramica dello spazio di archiviazione senza conferma</span><span class="sxs-lookup"><span data-stu-id="99971-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="99971-114">Il primo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace. Il secondo comando rimuove la panoramica dello spazio di archiviazione denominata MyStorageInsight da $Workspace senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="99971-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="99971-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99971-115">PARAMETERS</span></span>

### <span data-ttu-id="99971-116">-Force</span><span class="sxs-lookup"><span data-stu-id="99971-116">-Force</span></span>
<span data-ttu-id="99971-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99971-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99971-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="99971-118">-Name</span></span>
<span data-ttu-id="99971-119">Specifica il nome dell'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99971-119">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="99971-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99971-120">-ResourceGroupName</span></span>
<span data-ttu-id="99971-121">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="99971-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="99971-122">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="99971-122">-Workspace</span></span>
<span data-ttu-id="99971-123">Specifica l'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99971-123">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="99971-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99971-124">-WorkspaceName</span></span>
<span data-ttu-id="99971-125">Specifica il nome dell'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99971-125">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="99971-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99971-126">-Confirm</span></span>
<span data-ttu-id="99971-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99971-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99971-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99971-128">-WhatIf</span></span>
<span data-ttu-id="99971-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99971-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99971-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99971-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99971-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99971-131">-DefaultProfile</span></span>
<span data-ttu-id="99971-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99971-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99971-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99971-133">CommonParameters</span></span>
<span data-ttu-id="99971-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99971-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99971-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99971-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99971-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99971-136">INPUTS</span></span>

### <span data-ttu-id="99971-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="99971-137">PSWorkspace</span></span>
<span data-ttu-id="99971-138">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="99971-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="99971-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99971-139">OUTPUTS</span></span>

## <span data-ttu-id="99971-140">Note</span><span class="sxs-lookup"><span data-stu-id="99971-140">NOTES</span></span>

## <span data-ttu-id="99971-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99971-141">RELATED LINKS</span></span>

[<span data-ttu-id="99971-142">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="99971-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="99971-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="99971-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


