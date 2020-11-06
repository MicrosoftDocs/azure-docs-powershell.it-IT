---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519797"
---
# <span data-ttu-id="ad0a2-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="ad0a2-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="ad0a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0a2-103">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ad0a2-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad0a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad0a2-104">SYNTAX</span></span>

### <span data-ttu-id="ad0a2-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad0a2-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad0a2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0a2-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad0a2-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0a2-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0a2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad0a2-108">DESCRIPTION</span></span>
<span data-ttu-id="ad0a2-109">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ad0a2-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="ad0a2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad0a2-110">EXAMPLES</span></span>

### <span data-ttu-id="ad0a2-111">Elenca tutti i cluster di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ad0a2-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="ad0a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad0a2-112">PARAMETERS</span></span>

### <span data-ttu-id="ad0a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0a2-113">-DefaultProfile</span></span>
<span data-ttu-id="ad0a2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0a2-115">-ID</span><span class="sxs-lookup"><span data-stu-id="ad0a2-115">-Id</span></span>
<span data-ttu-id="ad0a2-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="ad0a2-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ad0a2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad0a2-117">-Name</span></span>
<span data-ttu-id="ad0a2-118">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="ad0a2-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ad0a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad0a2-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ad0a2-120">Resource group name</span></span>

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

### <span data-ttu-id="ad0a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0a2-121">CommonParameters</span></span>
<span data-ttu-id="ad0a2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0a2-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0a2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad0a2-124">INPUTS</span></span>

### <span data-ttu-id="ad0a2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0a2-125">System.String</span></span>

## <span data-ttu-id="ad0a2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad0a2-126">OUTPUTS</span></span>

### <span data-ttu-id="ad0a2-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ad0a2-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ad0a2-128">Note</span><span class="sxs-lookup"><span data-stu-id="ad0a2-128">NOTES</span></span>

## <span data-ttu-id="ad0a2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad0a2-129">RELATED LINKS</span></span>
