---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519692"
---
# <span data-ttu-id="64fe7-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="64fe7-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="64fe7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="64fe7-103">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="64fe7-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64fe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64fe7-104">SYNTAX</span></span>

### <span data-ttu-id="64fe7-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64fe7-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64fe7-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64fe7-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64fe7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="64fe7-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64fe7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="64fe7-109">Il **Get-AzureRmServiceFabricCluster** otterrà i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="64fe7-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="64fe7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="64fe7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64fe7-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="64fe7-112">Questo comando consente di ottenere i dettagli delle risorse del cluster per il cluster "raggruppamento".</span><span class="sxs-lookup"><span data-stu-id="64fe7-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="64fe7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64fe7-113">PARAMETERS</span></span>

### <span data-ttu-id="64fe7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64fe7-114">-DefaultProfile</span></span>
<span data-ttu-id="64fe7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64fe7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64fe7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="64fe7-116">-Name</span></span>
<span data-ttu-id="64fe7-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="64fe7-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="64fe7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64fe7-118">-ResourceGroupName</span></span>
<span data-ttu-id="64fe7-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64fe7-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64fe7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64fe7-120">CommonParameters</span></span>
<span data-ttu-id="64fe7-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64fe7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64fe7-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64fe7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64fe7-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64fe7-123">INPUTS</span></span>

### <span data-ttu-id="64fe7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="64fe7-124">System.String</span></span>

## <span data-ttu-id="64fe7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64fe7-125">OUTPUTS</span></span>

### <span data-ttu-id="64fe7-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="64fe7-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="64fe7-127">Note</span><span class="sxs-lookup"><span data-stu-id="64fe7-127">NOTES</span></span>

## <span data-ttu-id="64fe7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64fe7-128">RELATED LINKS</span></span>
