---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: 50d4dc8531f28ebb50ef562321b3974c7b50a102
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966941"
---
# <span data-ttu-id="fec65-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="fec65-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="fec65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec65-102">SYNOPSIS</span></span>
<span data-ttu-id="fec65-103">List Kubernetes managed clusters.</span><span class="sxs-lookup"><span data-stu-id="fec65-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="fec65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fec65-104">SYNTAX</span></span>

### <span data-ttu-id="fec65-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fec65-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fec65-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fec65-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fec65-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fec65-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fec65-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fec65-108">DESCRIPTION</span></span>
<span data-ttu-id="fec65-109">List Kubernetes managed clusters.</span><span class="sxs-lookup"><span data-stu-id="fec65-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="fec65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fec65-110">EXAMPLES</span></span>

### <span data-ttu-id="fec65-111">Elenca tutti i cluster Kubernetes</span><span class="sxs-lookup"><span data-stu-id="fec65-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="fec65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec65-112">PARAMETERS</span></span>

### <span data-ttu-id="fec65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec65-113">-DefaultProfile</span></span>
<span data-ttu-id="fec65-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fec65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec65-115">-Id</span><span class="sxs-lookup"><span data-stu-id="fec65-115">-Id</span></span>
<span data-ttu-id="fec65-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="fec65-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="fec65-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fec65-117">-Name</span></span>
<span data-ttu-id="fec65-118">Nome del cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="fec65-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="fec65-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec65-119">-ResourceGroupName</span></span>
<span data-ttu-id="fec65-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fec65-120">Resource group name</span></span>

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

### <span data-ttu-id="fec65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec65-121">CommonParameters</span></span>
<span data-ttu-id="fec65-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec65-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fec65-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec65-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="fec65-124">INPUTS</span></span>

### <span data-ttu-id="fec65-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fec65-125">System.String</span></span>

## <span data-ttu-id="fec65-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fec65-126">OUTPUTS</span></span>

### <span data-ttu-id="fec65-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fec65-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fec65-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="fec65-128">NOTES</span></span>

## <span data-ttu-id="fec65-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fec65-129">RELATED LINKS</span></span>
