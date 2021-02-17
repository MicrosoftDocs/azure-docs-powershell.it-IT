---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180598"
---
# <span data-ttu-id="43721-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="43721-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="43721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43721-102">SYNOPSIS</span></span>
<span data-ttu-id="43721-103">Consente il monitoraggio in un cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="43721-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="43721-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43721-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43721-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43721-105">DESCRIPTION</span></span>
<span data-ttu-id="43721-106">Il cmdlet **Enable-AzHDInsightMonitoring** abilita il monitoraggio in un cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43721-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="43721-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43721-107">EXAMPLES</span></span>

### <span data-ttu-id="43721-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43721-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="43721-109">Il monitoraggio verrà abilitato nel cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio con ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="43721-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="43721-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="43721-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="43721-111">Il monitoraggio verrà abilitato nel cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio con ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="43721-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="43721-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43721-112">PARAMETERS</span></span>

### <span data-ttu-id="43721-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43721-113">-DefaultProfile</span></span>
<span data-ttu-id="43721-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="43721-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43721-115">-Name</span><span class="sxs-lookup"><span data-stu-id="43721-115">-Name</span></span>
<span data-ttu-id="43721-116">Nome del cluster per abilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43721-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="43721-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="43721-117">-PrimaryKey</span></span>
<span data-ttu-id="43721-118">Chiave primaria dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43721-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="43721-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43721-119">-ResourceGroupName</span></span>
<span data-ttu-id="43721-120">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="43721-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="43721-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="43721-121">-WorkspaceId</span></span>
<span data-ttu-id="43721-122">ID dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43721-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="43721-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43721-123">-Confirm</span></span>
<span data-ttu-id="43721-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43721-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43721-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43721-125">-WhatIf</span></span>
<span data-ttu-id="43721-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43721-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43721-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43721-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43721-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43721-128">CommonParameters</span></span>
<span data-ttu-id="43721-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43721-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43721-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43721-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43721-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="43721-131">INPUTS</span></span>

### <span data-ttu-id="43721-132">System.String</span><span class="sxs-lookup"><span data-stu-id="43721-132">System.String</span></span>

## <span data-ttu-id="43721-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43721-133">OUTPUTS</span></span>

### <span data-ttu-id="43721-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43721-134">System.Boolean</span></span>

## <span data-ttu-id="43721-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="43721-135">NOTES</span></span>

## <span data-ttu-id="43721-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43721-136">RELATED LINKS</span></span>
