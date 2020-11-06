---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519548"
---
# <span data-ttu-id="7fc74-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7fc74-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="7fc74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fc74-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc74-103">Ottiene le definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fc74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fc74-104">SYNTAX</span></span>

### <span data-ttu-id="7fc74-105">Set di parametri per tutte le definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="7fc74-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="7fc74-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fc74-107">Set di parametri del nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc74-108">Set di parametri ID definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fc74-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fc74-109">DESCRIPTION</span></span>
<span data-ttu-id="7fc74-110">Il cmdlet **Get-AzureRmPolicySetDefinition** ottiene tutte le definizioni dei set di criteri o una definizione specifica del set di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="7fc74-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="7fc74-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fc74-111">EXAMPLES</span></span>

### <span data-ttu-id="7fc74-112">Esempio 1: ottenere tutte le definizioni di set di criteri</span><span class="sxs-lookup"><span data-stu-id="7fc74-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="7fc74-113">Questo comando ottiene tutte le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="7fc74-114">Esempio 2: ottenere la definizione del set di criteri per nome</span><span class="sxs-lookup"><span data-stu-id="7fc74-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="7fc74-115">Questo comando ottiene la definizione del set di criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7fc74-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="7fc74-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fc74-116">PARAMETERS</span></span>

### <span data-ttu-id="7fc74-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7fc74-117">-ApiVersion</span></span>
<span data-ttu-id="7fc74-118">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7fc74-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7fc74-119">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="7fc74-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7fc74-120">-ID</span><span class="sxs-lookup"><span data-stu-id="7fc74-120">-Id</span></span>
<span data-ttu-id="7fc74-121">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7fc74-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="7fc74-122">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="7fc74-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc74-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fc74-123">-Name</span></span>
<span data-ttu-id="7fc74-124">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="7fc74-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc74-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="7fc74-125">-Pre</span></span>
<span data-ttu-id="7fc74-126">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7fc74-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7fc74-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc74-127">-DefaultProfile</span></span>
<span data-ttu-id="7fc74-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc74-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fc74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc74-129">CommonParameters</span></span>
<span data-ttu-id="7fc74-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc74-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc74-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc74-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fc74-132">INPUTS</span></span>

### <span data-ttu-id="7fc74-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7fc74-133">System.String</span></span>

## <span data-ttu-id="7fc74-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fc74-134">OUTPUTS</span></span>

### <span data-ttu-id="7fc74-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7fc74-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7fc74-136">Note</span><span class="sxs-lookup"><span data-stu-id="7fc74-136">NOTES</span></span>

## <span data-ttu-id="7fc74-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fc74-137">RELATED LINKS</span></span>

