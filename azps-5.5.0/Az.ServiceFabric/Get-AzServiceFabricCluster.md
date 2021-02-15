---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197846"
---
# <span data-ttu-id="fe5ba-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fe5ba-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="fe5ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5ba-103">Informazioni dettagliate sulle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="fe5ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe5ba-104">SYNTAX</span></span>

### <span data-ttu-id="fe5ba-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe5ba-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5ba-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe5ba-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe5ba-107">ByName</span><span class="sxs-lookup"><span data-stu-id="fe5ba-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5ba-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe5ba-108">DESCRIPTION</span></span>
<span data-ttu-id="fe5ba-109">**Get-AzServiceFabricCluster riceverà** i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="fe5ba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe5ba-110">EXAMPLES</span></span>

### <span data-ttu-id="fe5ba-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe5ba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="fe5ba-112">Questo comando otterrà i dettagli della risorsa cluster per il cluster 'myCluster'.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="fe5ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe5ba-113">PARAMETERS</span></span>

### <span data-ttu-id="fe5ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5ba-114">-DefaultProfile</span></span>
<span data-ttu-id="fe5ba-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5ba-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fe5ba-116">-Name</span></span>
<span data-ttu-id="fe5ba-117">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="fe5ba-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fe5ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe5ba-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fe5ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5ba-120">CommonParameters</span></span>
<span data-ttu-id="fe5ba-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5ba-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fe5ba-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5ba-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe5ba-123">INPUTS</span></span>

### <span data-ttu-id="fe5ba-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fe5ba-124">System.String</span></span>

## <span data-ttu-id="fe5ba-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe5ba-125">OUTPUTS</span></span>

### <span data-ttu-id="fe5ba-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="fe5ba-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fe5ba-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe5ba-127">NOTES</span></span>

## <span data-ttu-id="fe5ba-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe5ba-128">RELATED LINKS</span></span>
