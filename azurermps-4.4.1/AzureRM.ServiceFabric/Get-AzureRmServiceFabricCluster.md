---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521526"
---
# <span data-ttu-id="869a0-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="869a0-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="869a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="869a0-102">SYNOPSIS</span></span>
<span data-ttu-id="869a0-103">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="869a0-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="869a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="869a0-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="869a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="869a0-105">DESCRIPTION</span></span>
<span data-ttu-id="869a0-106">Il **componente aggiuntivo AzureRmServiceFabricCluster** otterrà i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="869a0-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="869a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="869a0-107">EXAMPLES</span></span>

### <span data-ttu-id="869a0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="869a0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="869a0-109">Questo comando consente di ottenere i dettagli delle risorse del cluster per il cluster "raggruppamento".</span><span class="sxs-lookup"><span data-stu-id="869a0-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="869a0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="869a0-110">PARAMETERS</span></span>

### <span data-ttu-id="869a0-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="869a0-111">-Name</span></span>
<span data-ttu-id="869a0-112">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="869a0-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869a0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="869a0-113">-ResourceGroupName</span></span>
<span data-ttu-id="869a0-114">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="869a0-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869a0-115">-DefaultProfile</span></span>
<span data-ttu-id="869a0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="869a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869a0-117">CommonParameters</span></span>
<span data-ttu-id="869a0-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869a0-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869a0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="869a0-120">INPUTS</span></span>

### <span data-ttu-id="869a0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="869a0-121">System.String</span></span>

## <span data-ttu-id="869a0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="869a0-122">OUTPUTS</span></span>

### <span data-ttu-id="869a0-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. Commands. ServiceFabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="869a0-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="869a0-124">Note</span><span class="sxs-lookup"><span data-stu-id="869a0-124">NOTES</span></span>

## <span data-ttu-id="869a0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="869a0-125">RELATED LINKS</span></span>

