---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510352"
---
# <span data-ttu-id="af555-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="af555-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="af555-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af555-102">SYNOPSIS</span></span>
<span data-ttu-id="af555-103">Ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="af555-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af555-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af555-104">SYNTAX</span></span>

### <span data-ttu-id="af555-105">Elenco tutto il set di parametri delle applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="af555-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="af555-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="af555-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af555-107">Set di parametri del nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="af555-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af555-108">Set di parametri ID applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="af555-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af555-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af555-109">DESCRIPTION</span></span>
<span data-ttu-id="af555-110">Il cmdlet **Get-AzureRmManagedApplication** ottiene le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="af555-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="af555-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af555-111">EXAMPLES</span></span>

### <span data-ttu-id="af555-112">Esempio 1: ottenere tutte le applicazioni gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af555-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="af555-113">Questo comando consente di ottenere le applicazioni gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="af555-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="af555-114">Esempio 2: ottenere tutte le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="af555-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="af555-115">Questo comando ottiene tutte le applicazioni gestite in base alla sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="af555-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="af555-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af555-116">PARAMETERS</span></span>

### <span data-ttu-id="af555-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af555-117">-ApiVersion</span></span>
<span data-ttu-id="af555-118">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="af555-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="af555-119">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="af555-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="af555-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af555-120">-DefaultProfile</span></span>
<span data-ttu-id="af555-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af555-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af555-122">-ID</span><span class="sxs-lookup"><span data-stu-id="af555-122">-Id</span></span>
<span data-ttu-id="af555-123">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="af555-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="af555-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="af555-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af555-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="af555-125">-Name</span></span>
<span data-ttu-id="af555-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="af555-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af555-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="af555-127">-Pre</span></span>
<span data-ttu-id="af555-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="af555-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="af555-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af555-129">-ResourceGroupName</span></span>
<span data-ttu-id="af555-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af555-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af555-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af555-131">CommonParameters</span></span>
<span data-ttu-id="af555-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af555-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af555-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af555-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af555-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af555-134">INPUTS</span></span>

### <span data-ttu-id="af555-135">System. String</span><span class="sxs-lookup"><span data-stu-id="af555-135">System.String</span></span>

## <span data-ttu-id="af555-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af555-136">OUTPUTS</span></span>

### <span data-ttu-id="af555-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="af555-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="af555-138">Note</span><span class="sxs-lookup"><span data-stu-id="af555-138">NOTES</span></span>

## <span data-ttu-id="af555-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af555-139">RELATED LINKS</span></span>

