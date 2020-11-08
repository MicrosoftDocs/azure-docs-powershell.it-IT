---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193337"
---
# <span data-ttu-id="7d8cd-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="7d8cd-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="7d8cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8cd-103">Abilita il monitoraggio in un cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="7d8cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d8cd-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d8cd-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8cd-106">Il cmdlet **Enable-AzHDInsightMonitoring** Abilita il monitoraggio in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7d8cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d8cd-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8cd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d8cd-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="7d8cd-109">Il monitoraggio verrà abilitato nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro Monitoraggio con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7d8cd-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7d8cd-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d8cd-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="7d8cd-111">Il monitoraggio verrà abilitato nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro Monitoraggio con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7d8cd-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="7d8cd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d8cd-112">PARAMETERS</span></span>

### <span data-ttu-id="7d8cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8cd-113">-DefaultProfile</span></span>
<span data-ttu-id="7d8cd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d8cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d8cd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d8cd-115">-Name</span></span>
<span data-ttu-id="7d8cd-116">Il nome del cluster per abilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="7d8cd-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7d8cd-117">-PrimaryKey</span></span>
<span data-ttu-id="7d8cd-118">Chiave primaria dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="7d8cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d8cd-120">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="7d8cd-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7d8cd-121">-WorkspaceId</span></span>
<span data-ttu-id="7d8cd-122">ID dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="7d8cd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d8cd-123">-Confirm</span></span>
<span data-ttu-id="7d8cd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8cd-125">-WhatIf</span></span>
<span data-ttu-id="7d8cd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d8cd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8cd-128">CommonParameters</span></span>
<span data-ttu-id="7d8cd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8cd-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d8cd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8cd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d8cd-131">INPUTS</span></span>

### <span data-ttu-id="7d8cd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8cd-132">System.String</span></span>

## <span data-ttu-id="7d8cd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d8cd-133">OUTPUTS</span></span>

### <span data-ttu-id="7d8cd-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d8cd-134">System.Boolean</span></span>

## <span data-ttu-id="7d8cd-135">Note</span><span class="sxs-lookup"><span data-stu-id="7d8cd-135">NOTES</span></span>

## <span data-ttu-id="7d8cd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d8cd-136">RELATED LINKS</span></span>