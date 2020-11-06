---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519868"
---
# <span data-ttu-id="9be78-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9be78-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="9be78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9be78-102">SYNOPSIS</span></span>
<span data-ttu-id="9be78-103">Ottiene le definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="9be78-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9be78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9be78-104">SYNTAX</span></span>

### <span data-ttu-id="9be78-105">GetBySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9be78-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be78-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9be78-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be78-107">GetById</span><span class="sxs-lookup"><span data-stu-id="9be78-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be78-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9be78-108">DESCRIPTION</span></span>
<span data-ttu-id="9be78-109">Il cmdlet **Get-AzureRmPolicySetDefinition** ottiene tutte le definizioni dei set di criteri o una definizione specifica del set di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="9be78-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="9be78-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9be78-110">EXAMPLES</span></span>

### <span data-ttu-id="9be78-111">Esempio 1: ottenere tutte le definizioni di set di criteri</span><span class="sxs-lookup"><span data-stu-id="9be78-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="9be78-112">Questo comando ottiene tutte le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="9be78-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="9be78-113">Esempio 2: ottenere la definizione del set di criteri per nome</span><span class="sxs-lookup"><span data-stu-id="9be78-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="9be78-114">Questo comando ottiene la definizione del set di criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9be78-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="9be78-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9be78-115">PARAMETERS</span></span>

### <span data-ttu-id="9be78-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9be78-116">-ApiVersion</span></span>
<span data-ttu-id="9be78-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9be78-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9be78-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="9be78-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9be78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be78-119">-DefaultProfile</span></span>
<span data-ttu-id="9be78-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9be78-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9be78-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9be78-121">-Id</span></span>
<span data-ttu-id="9be78-122">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9be78-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="9be78-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9be78-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be78-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9be78-124">-Name</span></span>
<span data-ttu-id="9be78-125">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="9be78-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="9be78-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="9be78-126">-Pre</span></span>
<span data-ttu-id="9be78-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9be78-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9be78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be78-128">CommonParameters</span></span>
<span data-ttu-id="9be78-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be78-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be78-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be78-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9be78-131">INPUTS</span></span>

### <span data-ttu-id="9be78-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9be78-132">System.String</span></span>

## <span data-ttu-id="9be78-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9be78-133">OUTPUTS</span></span>

### <span data-ttu-id="9be78-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9be78-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9be78-135">Note</span><span class="sxs-lookup"><span data-stu-id="9be78-135">NOTES</span></span>

## <span data-ttu-id="9be78-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9be78-136">RELATED LINKS</span></span>
