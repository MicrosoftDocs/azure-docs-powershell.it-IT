---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 4f4508d38e4401198359fc816d1a94875f70940a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836060"
---
# <span data-ttu-id="b93f6-101">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="b93f6-101">Disable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="b93f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b93f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b93f6-103">Disabilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro OMS specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="b93f6-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="b93f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b93f6-104">SYNTAX</span></span>

```
Disable-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b93f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b93f6-106">Il cmdlet **Disable-AzHDInsightOperationsManagementSuite Disabilita** Operations Management Suite (OMS) in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="b93f6-106">The **Disable-AzHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b93f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b93f6-107">EXAMPLES</span></span>

### <span data-ttu-id="b93f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b93f6-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="b93f6-109">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="b93f6-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="b93f6-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b93f6-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="b93f6-111">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="b93f6-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="b93f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b93f6-112">PARAMETERS</span></span>

### <span data-ttu-id="b93f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93f6-113">-DefaultProfile</span></span>
<span data-ttu-id="b93f6-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b93f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b93f6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b93f6-115">-Name</span></span>
<span data-ttu-id="b93f6-116">Nome del cluster per disabilitare l'OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="b93f6-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="b93f6-118">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="b93f6-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="b93f6-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b93f6-119">-Confirm</span></span>
<span data-ttu-id="b93f6-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b93f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93f6-121">-WhatIf</span></span>
<span data-ttu-id="b93f6-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b93f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93f6-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b93f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93f6-124">CommonParameters</span></span>
<span data-ttu-id="b93f6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93f6-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93f6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b93f6-127">INPUTS</span></span>

### <span data-ttu-id="b93f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b93f6-128">System.String</span></span>

## <span data-ttu-id="b93f6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b93f6-129">OUTPUTS</span></span>

### <span data-ttu-id="b93f6-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="b93f6-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="b93f6-131">Note</span><span class="sxs-lookup"><span data-stu-id="b93f6-131">NOTES</span></span>

## <span data-ttu-id="b93f6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b93f6-132">RELATED LINKS</span></span>
