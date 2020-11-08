---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190719"
---
# <span data-ttu-id="70d78-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="70d78-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="70d78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70d78-102">SYNOPSIS</span></span>
<span data-ttu-id="70d78-103">Abilita il monitoraggio in un cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="70d78-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="70d78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70d78-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70d78-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70d78-105">DESCRIPTION</span></span>
<span data-ttu-id="70d78-106">Il cmdlet **Enable-AzHDInsightMonitoring** Abilita il monitoraggio in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="70d78-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70d78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70d78-107">EXAMPLES</span></span>

### <span data-ttu-id="70d78-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70d78-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="70d78-109">Il monitoraggio verrà abilitato nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro Monitoraggio con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="70d78-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="70d78-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="70d78-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="70d78-111">Il monitoraggio verrà abilitato nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro Monitoraggio con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="70d78-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="70d78-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70d78-112">PARAMETERS</span></span>

### <span data-ttu-id="70d78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d78-113">-DefaultProfile</span></span>
<span data-ttu-id="70d78-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="70d78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70d78-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="70d78-115">-Name</span></span>
<span data-ttu-id="70d78-116">Il nome del cluster per abilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="70d78-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="70d78-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="70d78-117">-PrimaryKey</span></span>
<span data-ttu-id="70d78-118">Chiave primaria dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="70d78-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="70d78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d78-119">-ResourceGroupName</span></span>
<span data-ttu-id="70d78-120">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="70d78-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="70d78-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="70d78-121">-WorkspaceId</span></span>
<span data-ttu-id="70d78-122">ID dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="70d78-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="70d78-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70d78-123">-Confirm</span></span>
<span data-ttu-id="70d78-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d78-125">-WhatIf</span></span>
<span data-ttu-id="70d78-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70d78-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70d78-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70d78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d78-128">CommonParameters</span></span>
<span data-ttu-id="70d78-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d78-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70d78-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d78-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70d78-131">INPUTS</span></span>

### <span data-ttu-id="70d78-132">System. String</span><span class="sxs-lookup"><span data-stu-id="70d78-132">System.String</span></span>

## <span data-ttu-id="70d78-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70d78-133">OUTPUTS</span></span>

### <span data-ttu-id="70d78-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70d78-134">System.Boolean</span></span>

## <span data-ttu-id="70d78-135">Note</span><span class="sxs-lookup"><span data-stu-id="70d78-135">NOTES</span></span>

## <span data-ttu-id="70d78-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70d78-136">RELATED LINKS</span></span>
