---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190654"
---
# <span data-ttu-id="1b8ab-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1b8ab-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="1b8ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8ab-103">Ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="1b8ab-103">Gets managed applications</span></span>

## <span data-ttu-id="1b8ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b8ab-104">SYNTAX</span></span>

### <span data-ttu-id="1b8ab-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b8ab-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b8ab-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1b8ab-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b8ab-107">GetById</span><span class="sxs-lookup"><span data-stu-id="1b8ab-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b8ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b8ab-108">DESCRIPTION</span></span>
<span data-ttu-id="1b8ab-109">Il cmdlet **Get-AzManagedApplication** ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="1b8ab-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="1b8ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b8ab-110">EXAMPLES</span></span>

### <span data-ttu-id="1b8ab-111">Esempio 1: ottenere tutte le applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1b8ab-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="1b8ab-112">Questo comando consente di ottenere le applicazioni gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="1b8ab-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="1b8ab-113">Esempio 2: ottenere tutte le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="1b8ab-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="1b8ab-114">Questo comando ottiene tutte le applicazioni gestite in base alla sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="1b8ab-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="1b8ab-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b8ab-115">PARAMETERS</span></span>

### <span data-ttu-id="1b8ab-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b8ab-116">-ApiVersion</span></span>
<span data-ttu-id="1b8ab-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b8ab-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1b8ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8ab-119">-DefaultProfile</span></span>
<span data-ttu-id="1b8ab-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b8ab-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1b8ab-121">-Id</span></span>
<span data-ttu-id="1b8ab-122">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="1b8ab-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1b8ab-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b8ab-124">-Name</span></span>
<span data-ttu-id="1b8ab-125">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ab-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b8ab-126">-Pre</span></span>
<span data-ttu-id="1b8ab-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b8ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b8ab-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8ab-130">CommonParameters</span></span>
<span data-ttu-id="1b8ab-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b8ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8ab-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b8ab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8ab-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b8ab-133">INPUTS</span></span>

### <span data-ttu-id="1b8ab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1b8ab-134">System.String</span></span>

## <span data-ttu-id="1b8ab-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b8ab-135">OUTPUTS</span></span>

### <span data-ttu-id="1b8ab-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b8ab-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b8ab-137">Note</span><span class="sxs-lookup"><span data-stu-id="1b8ab-137">NOTES</span></span>

## <span data-ttu-id="1b8ab-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b8ab-138">RELATED LINKS</span></span>
