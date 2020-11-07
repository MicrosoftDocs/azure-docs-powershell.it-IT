---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673713"
---
# <span data-ttu-id="f67e5-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="f67e5-101">Get-AzAks</span></span>

## <span data-ttu-id="f67e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f67e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f67e5-103">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f67e5-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f67e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f67e5-104">SYNTAX</span></span>

### <span data-ttu-id="f67e5-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f67e5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67e5-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f67e5-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67e5-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f67e5-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f67e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f67e5-108">DESCRIPTION</span></span>
<span data-ttu-id="f67e5-109">Elencare i cluster gestiti di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f67e5-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="f67e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f67e5-110">EXAMPLES</span></span>

### <span data-ttu-id="f67e5-111">Elenca tutti i cluster di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f67e5-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="f67e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f67e5-112">PARAMETERS</span></span>

### <span data-ttu-id="f67e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67e5-113">-DefaultProfile</span></span>
<span data-ttu-id="f67e5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f67e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f67e5-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f67e5-115">-Id</span></span>
<span data-ttu-id="f67e5-116">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f67e5-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f67e5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f67e5-117">-Name</span></span>
<span data-ttu-id="f67e5-118">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f67e5-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f67e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f67e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f67e5-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f67e5-120">Resource group name</span></span>

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

### <span data-ttu-id="f67e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67e5-121">CommonParameters</span></span>
<span data-ttu-id="f67e5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67e5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67e5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f67e5-124">INPUTS</span></span>

### <span data-ttu-id="f67e5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f67e5-125">System.String</span></span>

## <span data-ttu-id="f67e5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f67e5-126">OUTPUTS</span></span>

### <span data-ttu-id="f67e5-127">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f67e5-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f67e5-128">Note</span><span class="sxs-lookup"><span data-stu-id="f67e5-128">NOTES</span></span>

## <span data-ttu-id="f67e5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f67e5-129">RELATED LINKS</span></span>
