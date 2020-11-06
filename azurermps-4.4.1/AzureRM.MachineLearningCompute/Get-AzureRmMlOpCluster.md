---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519577"
---
# <span data-ttu-id="37cf8-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37cf8-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="37cf8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="37cf8-103">Ottiene un oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="37cf8-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37cf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37cf8-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37cf8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="37cf8-106">Ottiene un oggetto cluster di operatività per nome o per gruppo di risorse oppure per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="37cf8-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="37cf8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="37cf8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37cf8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="37cf8-109">Ottiene un cluster di operatività specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="37cf8-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="37cf8-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="37cf8-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="37cf8-111">Ottiene tutti i cluster di operatività in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37cf8-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="37cf8-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="37cf8-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="37cf8-113">Ottiene tutti i cluster di operatività in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="37cf8-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="37cf8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37cf8-114">PARAMETERS</span></span>

### <span data-ttu-id="37cf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cf8-115">-DefaultProfile</span></span>
<span data-ttu-id="37cf8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37cf8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37cf8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="37cf8-117">-Name</span></span>
<span data-ttu-id="37cf8-118">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="37cf8-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cf8-119">-ResourceGroupName</span></span>
<span data-ttu-id="37cf8-120">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="37cf8-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cf8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cf8-121">CommonParameters</span></span>
<span data-ttu-id="37cf8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cf8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cf8-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37cf8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cf8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37cf8-124">INPUTS</span></span>

### <span data-ttu-id="37cf8-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37cf8-125">None</span></span>

## <span data-ttu-id="37cf8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37cf8-126">OUTPUTS</span></span>

### <span data-ttu-id="37cf8-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="37cf8-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="37cf8-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="37cf8-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="37cf8-129">Note</span><span class="sxs-lookup"><span data-stu-id="37cf8-129">NOTES</span></span>

## <span data-ttu-id="37cf8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37cf8-130">RELATED LINKS</span></span>

