---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: ee8420a8869e1056dc0ee3d942b811c3f70d545d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519028"
---
# <span data-ttu-id="fdd36-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="fdd36-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="fdd36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdd36-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd36-103">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fdd36-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdd36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdd36-104">SYNTAX</span></span>

### <span data-ttu-id="fdd36-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdd36-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd36-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd36-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd36-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd36-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdd36-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdd36-108">DESCRIPTION</span></span>
<span data-ttu-id="fdd36-109">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fdd36-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="fdd36-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdd36-110">EXAMPLES</span></span>

### <span data-ttu-id="fdd36-111">Elenca tutti i cluster di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="fdd36-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="fdd36-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdd36-112">PARAMETERS</span></span>

### <span data-ttu-id="fdd36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd36-113">-DefaultProfile</span></span>
<span data-ttu-id="fdd36-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd36-115">-ID</span><span class="sxs-lookup"><span data-stu-id="fdd36-115">-Id</span></span>
<span data-ttu-id="fdd36-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="fdd36-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd36-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdd36-117">-Name</span></span>
<span data-ttu-id="fdd36-118">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="fdd36-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd36-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd36-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdd36-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fdd36-120">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd36-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd36-121">CommonParameters</span></span>
<span data-ttu-id="fdd36-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd36-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd36-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd36-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd36-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdd36-124">INPUTS</span></span>

### <span data-ttu-id="fdd36-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fdd36-125">System.String</span></span>

## <span data-ttu-id="fdd36-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdd36-126">OUTPUTS</span></span>

### <span data-ttu-id="fdd36-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fdd36-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="fdd36-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster, Microsoft. Azure. Commands. AKS, Version = 0.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fdd36-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster, Microsoft.Azure.Commands.Aks, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fdd36-129">Note</span><span class="sxs-lookup"><span data-stu-id="fdd36-129">NOTES</span></span>

## <span data-ttu-id="fdd36-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdd36-130">RELATED LINKS</span></span>
