---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: dc9e19c35f43b2420213d21b427d2aff69bb2541
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995538"
---
# <span data-ttu-id="ac1a3-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ac1a3-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="ac1a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1a3-103">Consente il monitoraggio in un cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="ac1a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac1a3-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac1a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1a3-106">Il cmdlet **Enable-AzHDInsightMonitoring** abilita il monitoraggio in un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ac1a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac1a3-107">EXAMPLES</span></span>

### <span data-ttu-id="ac1a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac1a3-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="ac1a3-109">Il monitoraggio verrà abilitato nel cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio con id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ac1a3-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ac1a3-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac1a3-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="ac1a3-111">Il monitoraggio verrà abilitato nel cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio con id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ac1a3-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="ac1a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac1a3-112">PARAMETERS</span></span>

### <span data-ttu-id="ac1a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1a3-113">-DefaultProfile</span></span>
<span data-ttu-id="ac1a3-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ac1a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac1a3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ac1a3-115">-Name</span></span>
<span data-ttu-id="ac1a3-116">Nome del cluster per abilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="ac1a3-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ac1a3-117">-PrimaryKey</span></span>
<span data-ttu-id="ac1a3-118">Chiave primaria dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac1a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac1a3-120">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="ac1a3-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ac1a3-121">-WorkspaceId</span></span>
<span data-ttu-id="ac1a3-122">ID dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1a3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac1a3-123">-Confirm</span></span>
<span data-ttu-id="ac1a3-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1a3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1a3-125">-WhatIf</span></span>
<span data-ttu-id="ac1a3-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac1a3-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1a3-128">CommonParameters</span></span>
<span data-ttu-id="ac1a3-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1a3-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1a3-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac1a3-131">INPUTS</span></span>

### <span data-ttu-id="ac1a3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ac1a3-132">System.String</span></span>

## <span data-ttu-id="ac1a3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac1a3-133">OUTPUTS</span></span>

### <span data-ttu-id="ac1a3-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac1a3-134">System.Boolean</span></span>

## <span data-ttu-id="ac1a3-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac1a3-135">NOTES</span></span>

## <span data-ttu-id="ac1a3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac1a3-136">RELATED LINKS</span></span>
