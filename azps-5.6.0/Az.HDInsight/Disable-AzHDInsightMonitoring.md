---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968990"
---
# <span data-ttu-id="1808e-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1808e-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="1808e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1808e-102">SYNOPSIS</span></span>
<span data-ttu-id="1808e-103">Disabilita il monitoraggio in un cluster HDInsight e il flusso dei log pertinenti nell'area di lavoro di monitoraggio specificata durante l'abilitazione non verrà più attivato.</span><span class="sxs-lookup"><span data-stu-id="1808e-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="1808e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1808e-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1808e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1808e-105">DESCRIPTION</span></span>
<span data-ttu-id="1808e-106">Il cmdlet **Disable-AzHDInsightMonitoring** disabilita il monitoraggio in un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1808e-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1808e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1808e-107">EXAMPLES</span></span>

### <span data-ttu-id="1808e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1808e-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="1808e-109">Il monitoraggio verrà disabilitato nel cluster HDInsight e i log pertinenti non verranno più efluiranno nell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1808e-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="1808e-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1808e-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="1808e-111">Il monitoraggio verrà disabilitato nel cluster HDInsight e i log pertinenti non verranno più efluiranno nell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1808e-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="1808e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1808e-112">PARAMETERS</span></span>

### <span data-ttu-id="1808e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1808e-113">-DefaultProfile</span></span>
<span data-ttu-id="1808e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1808e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1808e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1808e-115">-Name</span></span>
<span data-ttu-id="1808e-116">Nome del cluster per disabilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1808e-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1808e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1808e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1808e-118">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="1808e-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1808e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1808e-119">-Confirm</span></span>
<span data-ttu-id="1808e-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1808e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1808e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1808e-121">-WhatIf</span></span>
<span data-ttu-id="1808e-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1808e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1808e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1808e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1808e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1808e-124">CommonParameters</span></span>
<span data-ttu-id="1808e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1808e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1808e-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1808e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1808e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="1808e-127">INPUTS</span></span>

### <span data-ttu-id="1808e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1808e-128">System.String</span></span>

## <span data-ttu-id="1808e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1808e-129">OUTPUTS</span></span>

### <span data-ttu-id="1808e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1808e-130">System.Boolean</span></span>

## <span data-ttu-id="1808e-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="1808e-131">NOTES</span></span>

## <span data-ttu-id="1808e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1808e-132">RELATED LINKS</span></span>
