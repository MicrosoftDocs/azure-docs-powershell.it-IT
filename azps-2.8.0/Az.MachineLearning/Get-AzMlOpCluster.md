---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673941"
---
# <span data-ttu-id="82ecd-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="82ecd-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="82ecd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="82ecd-103">Ottiene un oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="82ecd-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="82ecd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82ecd-104">SYNTAX</span></span>

### <span data-ttu-id="82ecd-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="82ecd-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82ecd-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="82ecd-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ecd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="82ecd-108">Ottiene un oggetto cluster di operatività per nome o per gruppo di risorse oppure per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="82ecd-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="82ecd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="82ecd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82ecd-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="82ecd-111">Ottiene un cluster di operatività specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="82ecd-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="82ecd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="82ecd-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="82ecd-113">Ottiene tutti i cluster di operatività in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82ecd-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="82ecd-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="82ecd-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="82ecd-115">Ottiene tutti i cluster di operatività in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="82ecd-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="82ecd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82ecd-116">PARAMETERS</span></span>

### <span data-ttu-id="82ecd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ecd-117">-DefaultProfile</span></span>
<span data-ttu-id="82ecd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82ecd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ecd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="82ecd-119">-Name</span></span>
<span data-ttu-id="82ecd-120">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="82ecd-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ecd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ecd-121">-ResourceGroupName</span></span>
<span data-ttu-id="82ecd-122">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="82ecd-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ecd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ecd-123">CommonParameters</span></span>
<span data-ttu-id="82ecd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ecd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ecd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ecd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ecd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82ecd-126">INPUTS</span></span>

### <span data-ttu-id="82ecd-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82ecd-127">None</span></span>

## <span data-ttu-id="82ecd-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82ecd-128">OUTPUTS</span></span>

### <span data-ttu-id="82ecd-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="82ecd-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="82ecd-130">Note</span><span class="sxs-lookup"><span data-stu-id="82ecd-130">NOTES</span></span>

## <span data-ttu-id="82ecd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82ecd-131">RELATED LINKS</span></span>
