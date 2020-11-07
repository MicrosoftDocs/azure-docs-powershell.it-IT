---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686102"
---
# <span data-ttu-id="167bd-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="167bd-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="167bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="167bd-102">SYNOPSIS</span></span>
<span data-ttu-id="167bd-103">Ottiene un oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="167bd-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="167bd-104">SYNTAX</span></span>

### <span data-ttu-id="167bd-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="167bd-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="167bd-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="167bd-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="167bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="167bd-107">DESCRIPTION</span></span>
<span data-ttu-id="167bd-108">Ottiene un oggetto cluster di operatività per nome o per gruppo di risorse oppure per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="167bd-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="167bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="167bd-109">EXAMPLES</span></span>

### <span data-ttu-id="167bd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="167bd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="167bd-111">Ottiene un cluster di operatività specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="167bd-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="167bd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="167bd-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="167bd-113">Ottiene tutti i cluster di operatività in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="167bd-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="167bd-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="167bd-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="167bd-115">Ottiene tutti i cluster di operatività in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="167bd-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="167bd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="167bd-116">PARAMETERS</span></span>

### <span data-ttu-id="167bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167bd-117">-DefaultProfile</span></span>
<span data-ttu-id="167bd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="167bd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167bd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="167bd-119">-Name</span></span>
<span data-ttu-id="167bd-120">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="167bd-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="167bd-122">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="167bd-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167bd-123">CommonParameters</span></span>
<span data-ttu-id="167bd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167bd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167bd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="167bd-126">INPUTS</span></span>

### <span data-ttu-id="167bd-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="167bd-127">None</span></span>

## <span data-ttu-id="167bd-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="167bd-128">OUTPUTS</span></span>

### <span data-ttu-id="167bd-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="167bd-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="167bd-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="167bd-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="167bd-131">Note</span><span class="sxs-lookup"><span data-stu-id="167bd-131">NOTES</span></span>

## <span data-ttu-id="167bd-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="167bd-132">RELATED LINKS</span></span>
