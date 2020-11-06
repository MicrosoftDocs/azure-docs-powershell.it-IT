---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: dd0bb1bb72aa1193cba75c44905be37a70b62d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511520"
---
# <span data-ttu-id="0351f-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="0351f-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="0351f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0351f-102">SYNOPSIS</span></span>
<span data-ttu-id="0351f-103">Ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="0351f-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0351f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0351f-104">SYNTAX</span></span>

### <span data-ttu-id="0351f-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0351f-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0351f-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0351f-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0351f-107">GetById</span><span class="sxs-lookup"><span data-stu-id="0351f-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0351f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0351f-108">DESCRIPTION</span></span>
<span data-ttu-id="0351f-109">Il cmdlet **Get-AzureRmManagedApplication** ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="0351f-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="0351f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0351f-110">EXAMPLES</span></span>

### <span data-ttu-id="0351f-111">Esempio 1: ottenere tutte le applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0351f-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="0351f-112">Questo comando consente di ottenere le applicazioni gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="0351f-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="0351f-113">Esempio 2: ottenere tutte le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="0351f-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="0351f-114">Questo comando ottiene tutte le applicazioni gestite in base alla sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="0351f-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="0351f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0351f-115">PARAMETERS</span></span>

### <span data-ttu-id="0351f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0351f-116">-ApiVersion</span></span>
<span data-ttu-id="0351f-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="0351f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0351f-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="0351f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0351f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0351f-119">-DefaultProfile</span></span>
<span data-ttu-id="0351f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0351f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0351f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0351f-121">-Id</span></span>
<span data-ttu-id="0351f-122">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0351f-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="0351f-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0351f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="0351f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0351f-124">-Name</span></span>
<span data-ttu-id="0351f-125">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0351f-125">The managed application name.</span></span>

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

### <span data-ttu-id="0351f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0351f-126">-Pre</span></span>
<span data-ttu-id="0351f-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0351f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0351f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0351f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0351f-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0351f-129">The resource group name.</span></span>

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

### <span data-ttu-id="0351f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0351f-130">CommonParameters</span></span>
<span data-ttu-id="0351f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0351f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0351f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0351f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0351f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0351f-133">INPUTS</span></span>

### <span data-ttu-id="0351f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0351f-134">System.String</span></span>

## <span data-ttu-id="0351f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0351f-135">OUTPUTS</span></span>

### <span data-ttu-id="0351f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0351f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0351f-137">Note</span><span class="sxs-lookup"><span data-stu-id="0351f-137">NOTES</span></span>

## <span data-ttu-id="0351f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0351f-138">RELATED LINKS</span></span>
