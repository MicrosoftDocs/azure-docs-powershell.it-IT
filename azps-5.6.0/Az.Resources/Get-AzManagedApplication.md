---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008653"
---
# <span data-ttu-id="a2d34-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="a2d34-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="a2d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d34-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d34-103">Ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="a2d34-103">Gets managed applications</span></span>

## <span data-ttu-id="a2d34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2d34-104">SYNTAX</span></span>

### <span data-ttu-id="a2d34-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2d34-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2d34-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a2d34-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d34-107">GetById</span><span class="sxs-lookup"><span data-stu-id="a2d34-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d34-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2d34-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d34-109">Il cmdlet **Get-AzManagedApplication** ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="a2d34-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="a2d34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2d34-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d34-111">Esempio 1: Ottenere tutte le applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a2d34-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="a2d34-112">Questo comando recupera le applicazioni gestite nel gruppo di risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="a2d34-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="a2d34-113">Esempio 2: Ottenere tutte le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="a2d34-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="a2d34-114">Questo comando consente di ottenere tutte le applicazioni gestite nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="a2d34-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="a2d34-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2d34-115">PARAMETERS</span></span>

### <span data-ttu-id="a2d34-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a2d34-116">-ApiVersion</span></span>
<span data-ttu-id="a2d34-117">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a2d34-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a2d34-118">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="a2d34-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a2d34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d34-119">-DefaultProfile</span></span>
<span data-ttu-id="a2d34-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d34-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d34-121">-Id</span><span class="sxs-lookup"><span data-stu-id="a2d34-121">-Id</span></span>
<span data-ttu-id="a2d34-122">ID applicazione gestita completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a2d34-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="a2d34-123">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a2d34-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a2d34-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2d34-124">-Name</span></span>
<span data-ttu-id="a2d34-125">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a2d34-125">The managed application name.</span></span>

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

### <span data-ttu-id="a2d34-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="a2d34-126">-Pre</span></span>
<span data-ttu-id="a2d34-127">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a2d34-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a2d34-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d34-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2d34-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2d34-129">The resource group name.</span></span>

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

### <span data-ttu-id="a2d34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d34-130">CommonParameters</span></span>
<span data-ttu-id="a2d34-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d34-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2d34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d34-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2d34-133">INPUTS</span></span>

### <span data-ttu-id="a2d34-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a2d34-134">System.String</span></span>

## <span data-ttu-id="a2d34-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2d34-135">OUTPUTS</span></span>

### <span data-ttu-id="a2d34-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a2d34-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a2d34-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2d34-137">NOTES</span></span>

## <span data-ttu-id="a2d34-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2d34-138">RELATED LINKS</span></span>
