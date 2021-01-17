---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485900"
---
# <span data-ttu-id="0f919-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0f919-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="0f919-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f919-102">SYNOPSIS</span></span>
<span data-ttu-id="0f919-103">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="0f919-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="0f919-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f919-104">SYNTAX</span></span>

### <span data-ttu-id="0f919-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f919-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f919-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0f919-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f919-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0f919-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f919-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f919-108">DESCRIPTION</span></span>
<span data-ttu-id="0f919-109">Il **Get-AzServiceFabricCluster** otterrà i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="0f919-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="0f919-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f919-110">EXAMPLES</span></span>

### <span data-ttu-id="0f919-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f919-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="0f919-112">Questo comando consente di ottenere i dettagli delle risorse del cluster per il cluster "raggruppamento".</span><span class="sxs-lookup"><span data-stu-id="0f919-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="0f919-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f919-113">PARAMETERS</span></span>

### <span data-ttu-id="0f919-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f919-114">-DefaultProfile</span></span>
<span data-ttu-id="0f919-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f919-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f919-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f919-116">-Name</span></span>
<span data-ttu-id="0f919-117">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="0f919-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0f919-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f919-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f919-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f919-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0f919-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f919-120">CommonParameters</span></span>
<span data-ttu-id="0f919-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f919-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f919-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f919-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f919-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f919-123">INPUTS</span></span>

### <span data-ttu-id="0f919-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0f919-124">System.String</span></span>

## <span data-ttu-id="0f919-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f919-125">OUTPUTS</span></span>

### <span data-ttu-id="0f919-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0f919-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0f919-127">Note</span><span class="sxs-lookup"><span data-stu-id="0f919-127">NOTES</span></span>

## <span data-ttu-id="0f919-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f919-128">RELATED LINKS</span></span>
