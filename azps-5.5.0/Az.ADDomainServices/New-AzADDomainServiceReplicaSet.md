---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176591"
---
# <span data-ttu-id="c341d-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c341d-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="c341d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c341d-102">SYNOPSIS</span></span>
<span data-ttu-id="c341d-103">Creare un oggetto in memoria per ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c341d-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="c341d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c341d-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="c341d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c341d-105">DESCRIPTION</span></span>
<span data-ttu-id="c341d-106">Creare un oggetto in memoria per ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c341d-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="c341d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c341d-107">EXAMPLES</span></span>

### <span data-ttu-id="c341d-108">Esempio 1: Creare ReplicaSet per AdDomain</span><span class="sxs-lookup"><span data-stu-id="c341d-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="c341d-109">Create ReplicaSet for AdDomain</span><span class="sxs-lookup"><span data-stu-id="c341d-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="c341d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c341d-110">PARAMETERS</span></span>

### <span data-ttu-id="c341d-111">-Location</span><span class="sxs-lookup"><span data-stu-id="c341d-111">-Location</span></span>
<span data-ttu-id="c341d-112">Percorso di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c341d-112">Virtual network location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c341d-113">-SubnetId</span></span>
<span data-ttu-id="c341d-114">Nome della rete virtuale in cui verrà distribuito Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="c341d-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="c341d-115">ID della subnet in cui verranno distribuiti i Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="c341d-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="c341d-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="c341d-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c341d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c341d-117">CommonParameters</span></span>
<span data-ttu-id="c341d-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c341d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c341d-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c341d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c341d-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="c341d-120">INPUTS</span></span>

## <span data-ttu-id="c341d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c341d-121">OUTPUTS</span></span>

### <span data-ttu-id="c341d-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c341d-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="c341d-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="c341d-123">NOTES</span></span>

<span data-ttu-id="c341d-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c341d-124">ALIASES</span></span>

## <span data-ttu-id="c341d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c341d-125">RELATED LINKS</span></span>

