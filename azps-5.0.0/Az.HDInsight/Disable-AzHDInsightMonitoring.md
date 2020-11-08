---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193338"
---
# <span data-ttu-id="43347-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="43347-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="43347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43347-102">SYNOPSIS</span></span>
<span data-ttu-id="43347-103">Disabilita il monitoraggio in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="43347-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="43347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43347-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43347-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43347-105">DESCRIPTION</span></span>
<span data-ttu-id="43347-106">Il cmdlet **Disable-AzHDInsightMonitoring Disabilita** il monitoraggio in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="43347-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="43347-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43347-107">EXAMPLES</span></span>

### <span data-ttu-id="43347-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43347-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="43347-109">Il monitoraggio verrà disabilitato nel cluster HDInsight e i relativi registri verranno arrestati per l'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43347-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="43347-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="43347-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="43347-111">Il monitoraggio verrà disabilitato nel cluster HDInsight e i relativi registri verranno arrestati per l'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43347-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="43347-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43347-112">PARAMETERS</span></span>

### <span data-ttu-id="43347-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43347-113">-DefaultProfile</span></span>
<span data-ttu-id="43347-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="43347-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43347-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="43347-115">-Name</span></span>
<span data-ttu-id="43347-116">Nome del cluster per disabilitare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="43347-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="43347-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43347-117">-ResourceGroupName</span></span>
<span data-ttu-id="43347-118">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="43347-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="43347-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43347-119">-Confirm</span></span>
<span data-ttu-id="43347-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43347-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43347-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43347-121">-WhatIf</span></span>
<span data-ttu-id="43347-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43347-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43347-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43347-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43347-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43347-124">CommonParameters</span></span>
<span data-ttu-id="43347-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43347-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43347-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43347-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43347-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43347-127">INPUTS</span></span>

### <span data-ttu-id="43347-128">System. String</span><span class="sxs-lookup"><span data-stu-id="43347-128">System.String</span></span>

## <span data-ttu-id="43347-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43347-129">OUTPUTS</span></span>

### <span data-ttu-id="43347-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43347-130">System.Boolean</span></span>

## <span data-ttu-id="43347-131">Note</span><span class="sxs-lookup"><span data-stu-id="43347-131">NOTES</span></span>

## <span data-ttu-id="43347-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43347-132">RELATED LINKS</span></span>
