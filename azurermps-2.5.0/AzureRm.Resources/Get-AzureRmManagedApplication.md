---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 482bf9a2158fc299d78c993255e390dc480245a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866450"
---
# <span data-ttu-id="d8a30-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="d8a30-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="d8a30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8a30-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a30-103">Ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="d8a30-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8a30-104">SYNTAX</span></span>

### <span data-ttu-id="d8a30-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8a30-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8a30-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8a30-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8a30-107">GetById</span><span class="sxs-lookup"><span data-stu-id="d8a30-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8a30-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a30-109">Il cmdlet **Get-AzureRmManagedApplication** ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="d8a30-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="d8a30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8a30-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a30-111">Esempio 1: ottenere tutte le applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d8a30-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="d8a30-112">Questo comando consente di ottenere le applicazioni gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="d8a30-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="d8a30-113">Esempio 2: ottenere tutte le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="d8a30-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="d8a30-114">Questo comando ottiene tutte le applicazioni gestite in base alla sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="d8a30-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="d8a30-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8a30-115">PARAMETERS</span></span>

### <span data-ttu-id="d8a30-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8a30-116">-ApiVersion</span></span>
<span data-ttu-id="d8a30-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d8a30-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d8a30-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d8a30-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a30-119">-DefaultProfile</span></span>
<span data-ttu-id="d8a30-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a30-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8a30-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d8a30-121">-Id</span></span>
<span data-ttu-id="d8a30-122">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d8a30-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="d8a30-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d8a30-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a30-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8a30-124">-Name</span></span>
<span data-ttu-id="d8a30-125">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d8a30-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a30-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8a30-126">-Pre</span></span>
<span data-ttu-id="d8a30-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d8a30-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a30-128">-ResourceGroupName</span></span>
<span data-ttu-id="d8a30-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8a30-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a30-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a30-130">CommonParameters</span></span>
<span data-ttu-id="d8a30-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a30-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a30-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a30-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a30-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8a30-133">INPUTS</span></span>

### <span data-ttu-id="d8a30-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a30-134">System.String</span></span>

## <span data-ttu-id="d8a30-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8a30-135">OUTPUTS</span></span>

### <span data-ttu-id="d8a30-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d8a30-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d8a30-137">Note</span><span class="sxs-lookup"><span data-stu-id="d8a30-137">NOTES</span></span>

## <span data-ttu-id="d8a30-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8a30-138">RELATED LINKS</span></span>
