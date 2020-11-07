---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685874"
---
# <span data-ttu-id="b0a97-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b0a97-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="b0a97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0a97-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a97-103">Ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="b0a97-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0a97-104">SYNTAX</span></span>

### <span data-ttu-id="b0a97-105">Set di parametri del nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b0a97-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="b0a97-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="b0a97-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a97-107">Set di parametri ID definizione applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b0a97-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0a97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0a97-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a97-109">Il cmdlet **Get-AzureRmManagedApplicationDefinition** ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="b0a97-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="b0a97-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0a97-110">EXAMPLES</span></span>

### <span data-ttu-id="b0a97-111">Esempio 1: ottenere tutte le definizioni di applicazione gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b0a97-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="b0a97-112">Questo comando consente di ottenere le definizioni di applicazione gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="b0a97-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="b0a97-113">Esempio 2: ottenere una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="b0a97-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="b0a97-114">Questo comando ottiene la definizione dell'applicazione gestita "myManagedAppDef" in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="b0a97-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="b0a97-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0a97-115">PARAMETERS</span></span>

### <span data-ttu-id="b0a97-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b0a97-116">-ApiVersion</span></span>
<span data-ttu-id="b0a97-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b0a97-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b0a97-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="b0a97-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b0a97-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a97-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a97-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a97-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a97-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b0a97-121">-Id</span></span>
<span data-ttu-id="b0a97-122">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b0a97-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b0a97-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b0a97-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a97-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0a97-124">-Name</span></span>
<span data-ttu-id="b0a97-125">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b0a97-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a97-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b0a97-126">-Pre</span></span>
<span data-ttu-id="b0a97-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b0a97-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0a97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a97-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0a97-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0a97-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a97-130">CommonParameters</span></span>
<span data-ttu-id="b0a97-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a97-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a97-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a97-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0a97-133">INPUTS</span></span>

### <span data-ttu-id="b0a97-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b0a97-134">System.String</span></span>

## <span data-ttu-id="b0a97-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0a97-135">OUTPUTS</span></span>

### <span data-ttu-id="b0a97-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b0a97-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b0a97-137">Note</span><span class="sxs-lookup"><span data-stu-id="b0a97-137">NOTES</span></span>

## <span data-ttu-id="b0a97-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0a97-138">RELATED LINKS</span></span>

