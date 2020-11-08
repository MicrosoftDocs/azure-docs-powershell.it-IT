---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: f35cfcbfea4bdca0b75c2048fa403712c3262e02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022414"
---
# <span data-ttu-id="a0495-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a0495-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="a0495-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0495-102">SYNOPSIS</span></span>
<span data-ttu-id="a0495-103">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="a0495-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="a0495-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0495-104">SYNTAX</span></span>

### <span data-ttu-id="a0495-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0495-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0495-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0495-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0495-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a0495-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0495-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0495-108">DESCRIPTION</span></span>
<span data-ttu-id="a0495-109">Il **Get-AzServiceFabricCluster** otterrà i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="a0495-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="a0495-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0495-110">EXAMPLES</span></span>

### <span data-ttu-id="a0495-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0495-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="a0495-112">Questo comando consente di ottenere i dettagli delle risorse del cluster per il cluster "raggruppamento".</span><span class="sxs-lookup"><span data-stu-id="a0495-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="a0495-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0495-113">PARAMETERS</span></span>

### <span data-ttu-id="a0495-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0495-114">-DefaultProfile</span></span>
<span data-ttu-id="a0495-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0495-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0495-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0495-116">-Name</span></span>
<span data-ttu-id="a0495-117">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="a0495-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a0495-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0495-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0495-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0495-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a0495-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0495-120">CommonParameters</span></span>
<span data-ttu-id="a0495-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0495-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0495-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0495-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0495-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0495-123">INPUTS</span></span>

### <span data-ttu-id="a0495-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a0495-124">System.String</span></span>

## <span data-ttu-id="a0495-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0495-125">OUTPUTS</span></span>

### <span data-ttu-id="a0495-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a0495-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a0495-127">Note</span><span class="sxs-lookup"><span data-stu-id="a0495-127">NOTES</span></span>

## <span data-ttu-id="a0495-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0495-128">RELATED LINKS</span></span>
