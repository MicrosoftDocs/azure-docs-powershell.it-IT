---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473804"
---
# <span data-ttu-id="9a7c0-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="9a7c0-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="9a7c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7c0-103">Imposta le credenziali HTTP del gateway di un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9a7c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a7c0-104">SYNTAX</span></span>

### <span data-ttu-id="9a7c0-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a7c0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a7c0-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7c0-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a7c0-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7c0-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7c0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a7c0-108">DESCRIPTION</span></span>
<span data-ttu-id="9a7c0-109">Il cmdlet **set-AzHDInsightGatewayCredential** imposta le credenziali del gateway di un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9a7c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a7c0-110">EXAMPLES</span></span>

### <span data-ttu-id="9a7c0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a7c0-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9a7c0-112">Questo comando imposta le credenziali del gateway del cluster denominato set di parametri Hadoop-001 per nome.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="9a7c0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a7c0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9a7c0-114">Questo comando imposta le credenziali del gateway del cluster denominato your-Hadoop-001 by ResourceId set di parametri.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="9a7c0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9a7c0-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="9a7c0-116">Questo comando imposta le credenziali del gateway del cluster denominato your-Hadoop-001 by InputObject set di parametri.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="9a7c0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a7c0-117">PARAMETERS</span></span>

### <span data-ttu-id="9a7c0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a7c0-118">-AsJob</span></span>
<span data-ttu-id="9a7c0-119">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9a7c0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7c0-120">-DefaultProfile</span></span>
<span data-ttu-id="9a7c0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a7c0-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="9a7c0-122">-HttpCredential</span></span>
<span data-ttu-id="9a7c0-123">Ottiene o imposta l'account di accesso per l'utente del cluster.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="9a7c0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7c0-124">-InputObject</span></span>
<span data-ttu-id="9a7c0-125">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="9a7c0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a7c0-126">-Name</span></span>
<span data-ttu-id="9a7c0-127">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-127">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="9a7c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a7c0-129">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="9a7c0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a7c0-130">-ResourceId</span></span>
<span data-ttu-id="9a7c0-131">Ottiene o imposta l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="9a7c0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a7c0-132">-Confirm</span></span>
<span data-ttu-id="9a7c0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7c0-134">-WhatIf</span></span>
<span data-ttu-id="9a7c0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a7c0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7c0-137">CommonParameters</span></span>
<span data-ttu-id="9a7c0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7c0-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a7c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7c0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a7c0-140">INPUTS</span></span>

### <span data-ttu-id="9a7c0-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9a7c0-141">None</span></span>

## <span data-ttu-id="9a7c0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a7c0-142">OUTPUTS</span></span>

### <span data-ttu-id="9a7c0-143">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="9a7c0-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="9a7c0-144">Note</span><span class="sxs-lookup"><span data-stu-id="9a7c0-144">NOTES</span></span>

## <span data-ttu-id="9a7c0-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a7c0-145">RELATED LINKS</span></span>
