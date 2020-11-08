---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: d88ac0feab52d5f62a06981d8fa178db6dad9578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019931"
---
# <span data-ttu-id="f9fb5-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="f9fb5-101">Get-AzAks</span></span>

## <span data-ttu-id="f9fb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fb5-103">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f9fb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-104">SYNTAX</span></span>

### <span data-ttu-id="f9fb5-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9fb5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9fb5-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9fb5-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9fb5-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9fb5-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9fb5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9fb5-108">DESCRIPTION</span></span>
<span data-ttu-id="f9fb5-109">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f9fb5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-110">EXAMPLES</span></span>

### <span data-ttu-id="f9fb5-111">Elenca tutti i cluster di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f9fb5-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="f9fb5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-112">PARAMETERS</span></span>

### <span data-ttu-id="f9fb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fb5-113">-DefaultProfile</span></span>
<span data-ttu-id="f9fb5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9fb5-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f9fb5-115">-Id</span></span>
<span data-ttu-id="f9fb5-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f9fb5-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9fb5-117">-Name</span></span>
<span data-ttu-id="f9fb5-118">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f9fb5-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fb5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9fb5-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f9fb5-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fb5-121">CommonParameters</span></span>
<span data-ttu-id="f9fb5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fb5-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fb5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fb5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-124">INPUTS</span></span>

### <span data-ttu-id="f9fb5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f9fb5-125">System.String</span></span>

## <span data-ttu-id="f9fb5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9fb5-126">OUTPUTS</span></span>

### <span data-ttu-id="f9fb5-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f9fb5-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f9fb5-128">Note</span><span class="sxs-lookup"><span data-stu-id="f9fb5-128">NOTES</span></span>

## <span data-ttu-id="f9fb5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-129">RELATED LINKS</span></span>
