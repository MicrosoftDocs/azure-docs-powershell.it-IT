---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516083"
---
# <span data-ttu-id="de9e6-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="de9e6-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="de9e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="de9e6-103">Modifica di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="de9e6-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de9e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de9e6-104">SYNTAX</span></span>

### <span data-ttu-id="de9e6-105">Set di parametri del nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="de9e6-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="de9e6-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de9e6-107">Set di parametri ID definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de9e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de9e6-108">DESCRIPTION</span></span>
<span data-ttu-id="de9e6-109">Il cmdlet **set-AzureRmPolicySetDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="de9e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de9e6-110">EXAMPLES</span></span>

### <span data-ttu-id="de9e6-111">Esempio 1: aggiornare la descrizione di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="de9e6-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="de9e6-112">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="de9e6-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="de9e6-113">Il comando Archivia l'oggetto nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="de9e6-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="de9e6-114">Il secondo comando Aggiorna la descrizione della definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="de9e6-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="de9e6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de9e6-115">PARAMETERS</span></span>

### <span data-ttu-id="de9e6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de9e6-116">-ApiVersion</span></span>
<span data-ttu-id="de9e6-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="de9e6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="de9e6-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="de9e6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="de9e6-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="de9e6-119">-Description</span></span>
<span data-ttu-id="de9e6-120">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-120">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9e6-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de9e6-121">-DisplayName</span></span>
<span data-ttu-id="de9e6-122">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-122">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9e6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="de9e6-123">-Id</span></span>
<span data-ttu-id="de9e6-124">ID di definizione dei criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="de9e6-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="de9e6-125">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="de9e6-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="de9e6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="de9e6-126">-Name</span></span>
<span data-ttu-id="de9e6-127">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-127">The policy set definition name.</span></span>

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

### <span data-ttu-id="de9e6-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="de9e6-128">-PolicyDefinition</span></span>
<span data-ttu-id="de9e6-129">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="de9e6-129">The policy set definition.</span></span> <span data-ttu-id="de9e6-130">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="de9e6-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9e6-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="de9e6-131">-Pre</span></span>
<span data-ttu-id="de9e6-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="de9e6-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de9e6-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de9e6-133">-Confirm</span></span>
<span data-ttu-id="de9e6-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de9e6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9e6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9e6-135">-DefaultProfile</span></span>
<span data-ttu-id="de9e6-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de9e6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de9e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de9e6-137">-WhatIf</span></span>
<span data-ttu-id="de9e6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de9e6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de9e6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de9e6-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9e6-140">CommonParameters</span></span>
<span data-ttu-id="de9e6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9e6-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de9e6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9e6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de9e6-143">INPUTS</span></span>

### <span data-ttu-id="de9e6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="de9e6-144">System.String</span></span>

## <span data-ttu-id="de9e6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de9e6-145">OUTPUTS</span></span>

### <span data-ttu-id="de9e6-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="de9e6-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="de9e6-147">Note</span><span class="sxs-lookup"><span data-stu-id="de9e6-147">NOTES</span></span>

## <span data-ttu-id="de9e6-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de9e6-148">RELATED LINKS</span></span>

