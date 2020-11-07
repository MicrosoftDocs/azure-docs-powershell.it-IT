---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674327"
---
# <span data-ttu-id="9bdcd-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9bdcd-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="9bdcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bdcd-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdcd-103">Abilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro OMS specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="9bdcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bdcd-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bdcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bdcd-105">DESCRIPTION</span></span>
<span data-ttu-id="9bdcd-106">Il cmdlet **Enable-AzHDInsightOperationsManagementSuite** consente a Operations Management Suite (OMS) in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9bdcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bdcd-107">EXAMPLES</span></span>

### <span data-ttu-id="9bdcd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bdcd-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="9bdcd-109">Le Operations Management Suite (OMS) verranno abilitate nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro OMS con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="9bdcd-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="9bdcd-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9bdcd-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="9bdcd-111">Le Operations Management Suite (OMS) verranno abilitate nel cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro OMS con ID 1d364e89-BB71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="9bdcd-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="9bdcd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bdcd-112">PARAMETERS</span></span>

### <span data-ttu-id="9bdcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdcd-113">-DefaultProfile</span></span>
<span data-ttu-id="9bdcd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9bdcd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bdcd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bdcd-115">-Name</span></span>
<span data-ttu-id="9bdcd-116">Il nome del cluster per abilitare le Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="9bdcd-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="9bdcd-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9bdcd-117">-PrimaryKey</span></span>
<span data-ttu-id="9bdcd-118">Chiave primaria dell'area di lavoro OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="9bdcd-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="9bdcd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bdcd-119">-ResourceGroupName</span></span>
<span data-ttu-id="9bdcd-120">Gruppo di risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="9bdcd-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9bdcd-121">-WorkspaceId</span></span>
<span data-ttu-id="9bdcd-122">ID dell'area di lavoro OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="9bdcd-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="9bdcd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bdcd-123">-Confirm</span></span>
<span data-ttu-id="9bdcd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bdcd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdcd-125">-WhatIf</span></span>
<span data-ttu-id="9bdcd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bdcd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bdcd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdcd-128">CommonParameters</span></span>
<span data-ttu-id="9bdcd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdcd-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bdcd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdcd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bdcd-131">INPUTS</span></span>

### <span data-ttu-id="9bdcd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9bdcd-132">System.String</span></span>

## <span data-ttu-id="9bdcd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bdcd-133">OUTPUTS</span></span>

### <span data-ttu-id="9bdcd-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="9bdcd-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="9bdcd-135">Note</span><span class="sxs-lookup"><span data-stu-id="9bdcd-135">NOTES</span></span>

## <span data-ttu-id="9bdcd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bdcd-136">RELATED LINKS</span></span>
