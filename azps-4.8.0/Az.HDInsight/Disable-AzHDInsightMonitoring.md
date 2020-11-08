---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190718"
---
# <span data-ttu-id="6dce0-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="6dce0-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="6dce0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dce0-102">SYNOPSIS</span></span>
<span data-ttu-id="6dce0-103">Disabilita il monitoraggio in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="6dce0-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="6dce0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dce0-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dce0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dce0-105">DESCRIPTION</span></span>
<span data-ttu-id="6dce0-106">Il cmdlet **Disable-AzHDInsightMonitoring Disabilita** il monitoraggio in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="6dce0-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6dce0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dce0-107">EXAMPLES</span></span>

### <span data-ttu-id="6dce0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6dce0-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="6dce0-109">Il monitoraggio verrà disabilitato nel cluster HDInsight e i relativi registri verranno arrestati per l'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6dce0-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="6dce0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6dce0-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="6dce0-111">Il monitoraggio verrà disabilitato nel cluster HDInsight e i relativi registri verranno arrestati per l'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6dce0-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="6dce0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dce0-112">PARAMETERS</span></span>

### <span data-ttu-id="6dce0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dce0-113">-DefaultProfile</span></span>
<span data-ttu-id="6dce0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6dce0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dce0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dce0-115">-Name</span></span>
<span data-ttu-id="6dce0-116">Nome del cluster per disabilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6dce0-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="6dce0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dce0-117">-ResourceGroupName</span></span>
<span data-ttu-id="6dce0-118">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="6dce0-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="6dce0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6dce0-119">-Confirm</span></span>
<span data-ttu-id="6dce0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dce0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dce0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dce0-121">-WhatIf</span></span>
<span data-ttu-id="6dce0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dce0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dce0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dce0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dce0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dce0-124">CommonParameters</span></span>
<span data-ttu-id="6dce0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dce0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dce0-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dce0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dce0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dce0-127">INPUTS</span></span>

### <span data-ttu-id="6dce0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6dce0-128">System.String</span></span>

## <span data-ttu-id="6dce0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dce0-129">OUTPUTS</span></span>

### <span data-ttu-id="6dce0-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dce0-130">System.Boolean</span></span>

## <span data-ttu-id="6dce0-131">Note</span><span class="sxs-lookup"><span data-stu-id="6dce0-131">NOTES</span></span>

## <span data-ttu-id="6dce0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dce0-132">RELATED LINKS</span></span>