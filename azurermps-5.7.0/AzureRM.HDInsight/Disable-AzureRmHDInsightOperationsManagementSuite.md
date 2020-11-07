---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518116"
---
# <span data-ttu-id="95c03-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="95c03-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="95c03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95c03-102">SYNOPSIS</span></span>
<span data-ttu-id="95c03-103">Disabilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro OMS specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="95c03-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95c03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95c03-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c03-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95c03-105">DESCRIPTION</span></span>
<span data-ttu-id="95c03-106">Il cmdlet **Disable-AzureRmHDInsightOperationsManagementSuite Disabilita** Operations Management Suite (OMS) in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="95c03-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="95c03-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95c03-107">EXAMPLES</span></span>

### <span data-ttu-id="95c03-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95c03-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="95c03-109">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="95c03-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="95c03-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="95c03-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="95c03-111">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="95c03-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="95c03-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95c03-112">PARAMETERS</span></span>

### <span data-ttu-id="95c03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c03-113">-DefaultProfile</span></span>
<span data-ttu-id="95c03-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="95c03-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c03-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="95c03-115">-Name</span></span>
<span data-ttu-id="95c03-116">Nome del cluster per disabilitare l'OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="95c03-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95c03-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c03-117">-ResourceGroupName</span></span>
<span data-ttu-id="95c03-118">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="95c03-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c03-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95c03-119">-Confirm</span></span>
<span data-ttu-id="95c03-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95c03-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c03-121">-WhatIf</span></span>
<span data-ttu-id="95c03-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95c03-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95c03-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95c03-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c03-124">CommonParameters</span></span>
<span data-ttu-id="95c03-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c03-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c03-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c03-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95c03-127">INPUTS</span></span>

### <span data-ttu-id="95c03-128">System. String</span><span class="sxs-lookup"><span data-stu-id="95c03-128">System.String</span></span>

## <span data-ttu-id="95c03-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95c03-129">OUTPUTS</span></span>

### <span data-ttu-id="95c03-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="95c03-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="95c03-131">Note</span><span class="sxs-lookup"><span data-stu-id="95c03-131">NOTES</span></span>

## <span data-ttu-id="95c03-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95c03-132">RELATED LINKS</span></span>
