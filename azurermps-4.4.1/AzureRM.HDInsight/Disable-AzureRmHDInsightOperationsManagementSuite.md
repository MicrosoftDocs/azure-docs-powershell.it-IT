---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7a4488c606206c1a5a6043140abfbd125cc6b21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519180"
---
# <span data-ttu-id="39e4b-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="39e4b-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="39e4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="39e4b-103">Disabilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro OMS specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="39e4b-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39e4b-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39e4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="39e4b-106">Il cmdlet **Disable-AzureRmHDInsightOperationsManagementSuite Disabilita** Operations Management Suite (OMS) in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="39e4b-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="39e4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39e4b-107">EXAMPLES</span></span>

### <span data-ttu-id="39e4b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39e4b-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="39e4b-109">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="39e4b-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="39e4b-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="39e4b-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="39e4b-111">Le Operations Management Suite (OMS) verranno disabilitate nel cluster HDInsight e i registri rilevanti smetteranno di scorrere verso l'area di lavoro OMS.</span><span class="sxs-lookup"><span data-stu-id="39e4b-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="39e4b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39e4b-112">PARAMETERS</span></span>

### <span data-ttu-id="39e4b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="39e4b-113">-Name</span></span>
<span data-ttu-id="39e4b-114">Nome del cluster per disabilitare l'OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="39e4b-114">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="39e4b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e4b-115">-ResourceGroupName</span></span>
<span data-ttu-id="39e4b-116">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="39e4b-116">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="39e4b-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39e4b-117">-Confirm</span></span>
<span data-ttu-id="39e4b-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39e4b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e4b-119">-DefaultProfile</span></span>
<span data-ttu-id="39e4b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39e4b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e4b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e4b-121">-WhatIf</span></span>
<span data-ttu-id="39e4b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39e4b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39e4b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39e4b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e4b-124">CommonParameters</span></span>
<span data-ttu-id="39e4b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e4b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e4b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e4b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39e4b-127">INPUTS</span></span>

### <span data-ttu-id="39e4b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="39e4b-128">System.String</span></span>

## <span data-ttu-id="39e4b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39e4b-129">OUTPUTS</span></span>

### <span data-ttu-id="39e4b-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="39e4b-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="39e4b-131">Note</span><span class="sxs-lookup"><span data-stu-id="39e4b-131">NOTES</span></span>

## <span data-ttu-id="39e4b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39e4b-132">RELATED LINKS</span></span>

