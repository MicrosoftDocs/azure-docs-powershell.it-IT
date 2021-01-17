---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479124"
---
# <span data-ttu-id="166bf-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="166bf-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="166bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="166bf-102">SYNOPSIS</span></span>
<span data-ttu-id="166bf-103">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="166bf-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="166bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="166bf-104">SYNTAX</span></span>

### <span data-ttu-id="166bf-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="166bf-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="166bf-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="166bf-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="166bf-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="166bf-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="166bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="166bf-108">DESCRIPTION</span></span>
<span data-ttu-id="166bf-109">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="166bf-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="166bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="166bf-110">EXAMPLES</span></span>

### <span data-ttu-id="166bf-111">Elenca tutti i cluster di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="166bf-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="166bf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="166bf-112">PARAMETERS</span></span>

### <span data-ttu-id="166bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166bf-113">-DefaultProfile</span></span>
<span data-ttu-id="166bf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="166bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166bf-115">-ID</span><span class="sxs-lookup"><span data-stu-id="166bf-115">-Id</span></span>
<span data-ttu-id="166bf-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="166bf-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="166bf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="166bf-117">-Name</span></span>
<span data-ttu-id="166bf-118">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="166bf-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="166bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="166bf-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="166bf-120">Resource group name</span></span>

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

### <span data-ttu-id="166bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166bf-121">CommonParameters</span></span>
<span data-ttu-id="166bf-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166bf-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="166bf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166bf-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="166bf-124">INPUTS</span></span>

### <span data-ttu-id="166bf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="166bf-125">System.String</span></span>

## <span data-ttu-id="166bf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="166bf-126">OUTPUTS</span></span>

### <span data-ttu-id="166bf-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="166bf-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="166bf-128">Note</span><span class="sxs-lookup"><span data-stu-id="166bf-128">NOTES</span></span>

## <span data-ttu-id="166bf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="166bf-129">RELATED LINKS</span></span>
