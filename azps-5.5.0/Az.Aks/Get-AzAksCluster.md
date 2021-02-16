---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199886"
---
# <span data-ttu-id="903bb-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="903bb-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="903bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903bb-102">SYNOPSIS</span></span>
<span data-ttu-id="903bb-103">List Kubernetes managed clusters.</span><span class="sxs-lookup"><span data-stu-id="903bb-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="903bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="903bb-104">SYNTAX</span></span>

### <span data-ttu-id="903bb-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="903bb-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="903bb-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="903bb-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903bb-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="903bb-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="903bb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="903bb-108">DESCRIPTION</span></span>
<span data-ttu-id="903bb-109">List Kubernetes managed clusters.</span><span class="sxs-lookup"><span data-stu-id="903bb-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="903bb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="903bb-110">EXAMPLES</span></span>

### <span data-ttu-id="903bb-111">Elenca tutti i cluster Kubernetes</span><span class="sxs-lookup"><span data-stu-id="903bb-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="903bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="903bb-112">PARAMETERS</span></span>

### <span data-ttu-id="903bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903bb-113">-DefaultProfile</span></span>
<span data-ttu-id="903bb-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="903bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903bb-115">-Id</span><span class="sxs-lookup"><span data-stu-id="903bb-115">-Id</span></span>
<span data-ttu-id="903bb-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="903bb-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="903bb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="903bb-117">-Name</span></span>
<span data-ttu-id="903bb-118">Nome del cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="903bb-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="903bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="903bb-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="903bb-120">Resource group name</span></span>

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

### <span data-ttu-id="903bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903bb-121">CommonParameters</span></span>
<span data-ttu-id="903bb-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903bb-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="903bb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903bb-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="903bb-124">INPUTS</span></span>

### <span data-ttu-id="903bb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="903bb-125">System.String</span></span>

## <span data-ttu-id="903bb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="903bb-126">OUTPUTS</span></span>

### <span data-ttu-id="903bb-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="903bb-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="903bb-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="903bb-128">NOTES</span></span>

## <span data-ttu-id="903bb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="903bb-129">RELATED LINKS</span></span>
