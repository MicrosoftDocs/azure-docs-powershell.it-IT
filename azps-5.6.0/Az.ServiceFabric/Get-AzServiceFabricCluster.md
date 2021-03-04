---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955645"
---
# <span data-ttu-id="6c2cc-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6c2cc-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="6c2cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2cc-103">Informazioni dettagliate sulle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="6c2cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c2cc-104">SYNTAX</span></span>

### <span data-ttu-id="6c2cc-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c2cc-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c2cc-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c2cc-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c2cc-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6c2cc-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c2cc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c2cc-108">DESCRIPTION</span></span>
<span data-ttu-id="6c2cc-109">**Get-AzServiceFabricCluster riceverà** i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="6c2cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c2cc-110">EXAMPLES</span></span>

### <span data-ttu-id="6c2cc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c2cc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="6c2cc-112">Questo comando otterrà i dettagli della risorsa cluster per il cluster 'myCluster'.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="6c2cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c2cc-113">PARAMETERS</span></span>

### <span data-ttu-id="6c2cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2cc-114">-DefaultProfile</span></span>
<span data-ttu-id="6c2cc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2cc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6c2cc-116">-Name</span></span>
<span data-ttu-id="6c2cc-117">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="6c2cc-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2cc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2cc-118">-ResourceGroupName</span></span>
<span data-ttu-id="6c2cc-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2cc-120">CommonParameters</span></span>
<span data-ttu-id="6c2cc-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2cc-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c2cc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2cc-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c2cc-123">INPUTS</span></span>

### <span data-ttu-id="6c2cc-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6c2cc-124">System.String</span></span>

## <span data-ttu-id="6c2cc-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c2cc-125">OUTPUTS</span></span>

### <span data-ttu-id="6c2cc-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6c2cc-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6c2cc-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c2cc-127">NOTES</span></span>

## <span data-ttu-id="6c2cc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c2cc-128">RELATED LINKS</span></span>
