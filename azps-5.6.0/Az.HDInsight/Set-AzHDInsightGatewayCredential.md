---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: e864e963e91df9599642c763a151325dd68d65a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986045"
---
# <span data-ttu-id="5ab05-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="5ab05-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="5ab05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab05-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab05-103">Imposta le credenziali HTTP del gateway di un cluster HdInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab05-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5ab05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ab05-104">SYNTAX</span></span>

### <span data-ttu-id="5ab05-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ab05-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ab05-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ab05-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ab05-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ab05-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab05-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ab05-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab05-109">Il cmdlet **Set-AzHDInsightGatewayCredential** imposta le credenziali del gateway di un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5ab05-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5ab05-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ab05-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab05-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ab05-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="5ab05-112">Questo comando imposta le credenziali del gateway del cluster denominato your-hadoop-001 in base al set di parametri del nome.</span><span class="sxs-lookup"><span data-stu-id="5ab05-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="5ab05-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5ab05-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="5ab05-114">Questo comando imposta le credenziali del gateway del cluster denominato your-hadoop-001 in base al set di parametri ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5ab05-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="5ab05-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5ab05-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="5ab05-116">Questo comando imposta le credenziali del gateway del cluster denominato your-hadoop-001 in base al set di parametri InputObject.</span><span class="sxs-lookup"><span data-stu-id="5ab05-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="5ab05-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ab05-117">PARAMETERS</span></span>

### <span data-ttu-id="5ab05-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ab05-118">-AsJob</span></span>
<span data-ttu-id="5ab05-119">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="5ab05-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="5ab05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab05-120">-DefaultProfile</span></span>
<span data-ttu-id="5ab05-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab05-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5ab05-122">-HttpCredential</span></span>
<span data-ttu-id="5ab05-123">Ottiene o imposta l'accesso per l'utente del cluster.</span><span class="sxs-lookup"><span data-stu-id="5ab05-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ab05-124">-InputObject</span></span>
<span data-ttu-id="5ab05-125">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="5ab05-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5ab05-126">-Name</span></span>
<span data-ttu-id="5ab05-127">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="5ab05-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab05-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ab05-129">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ab05-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab05-130">-ResourceId</span></span>
<span data-ttu-id="5ab05-131">Ottiene o imposta l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ab05-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ab05-132">-Confirm</span></span>
<span data-ttu-id="5ab05-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab05-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab05-134">-WhatIf</span></span>
<span data-ttu-id="5ab05-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ab05-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ab05-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ab05-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab05-137">CommonParameters</span></span>
<span data-ttu-id="5ab05-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab05-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ab05-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab05-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ab05-140">INPUTS</span></span>

### <span data-ttu-id="5ab05-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5ab05-141">None</span></span>

## <span data-ttu-id="5ab05-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ab05-142">OUTPUTS</span></span>

### <span data-ttu-id="5ab05-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="5ab05-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="5ab05-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ab05-144">NOTES</span></span>

## <span data-ttu-id="5ab05-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ab05-145">RELATED LINKS</span></span>
