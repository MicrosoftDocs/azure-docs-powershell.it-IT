---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 41cf22aab3cc79499d5a2c8918197c1cd6d092e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866968"
---
# <span data-ttu-id="38f6d-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="38f6d-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="38f6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="38f6d-103">Rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="38f6d-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38f6d-104">SYNTAX</span></span>

### <span data-ttu-id="38f6d-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38f6d-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38f6d-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="38f6d-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f6d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38f6d-107">DESCRIPTION</span></span>
<span data-ttu-id="38f6d-108">Il cmdlet **Remove-AzureRmManagedApplicationDefinition** rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="38f6d-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="38f6d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38f6d-109">EXAMPLES</span></span>

### <span data-ttu-id="38f6d-110">Esempio 1: rimuovere la definizione di applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="38f6d-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="38f6d-111">Il primo comando ottiene una definizione di applicazione gestita denominata myAppDef tramite il cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="38f6d-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="38f6d-112">Il comando lo archivia nella variabile $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="38f6d-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="38f6d-113">Il secondo comando rimuove la definizione dell'applicazione gestita identificata dalla proprietà **resourceId** di $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="38f6d-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="38f6d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38f6d-114">PARAMETERS</span></span>

### <span data-ttu-id="38f6d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38f6d-115">-ApiVersion</span></span>
<span data-ttu-id="38f6d-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="38f6d-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="38f6d-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="38f6d-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="38f6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f6d-118">-DefaultProfile</span></span>
<span data-ttu-id="38f6d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38f6d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f6d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="38f6d-120">-Force</span></span>
<span data-ttu-id="38f6d-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="38f6d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38f6d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="38f6d-122">-Id</span></span>
<span data-ttu-id="38f6d-123">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="38f6d-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="38f6d-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="38f6d-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f6d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="38f6d-125">-Name</span></span>
<span data-ttu-id="38f6d-126">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="38f6d-126">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f6d-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="38f6d-127">-Pre</span></span>
<span data-ttu-id="38f6d-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="38f6d-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="38f6d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f6d-129">-ResourceGroupName</span></span>
<span data-ttu-id="38f6d-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38f6d-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f6d-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38f6d-131">-Confirm</span></span>
<span data-ttu-id="38f6d-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f6d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f6d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f6d-133">-WhatIf</span></span>
<span data-ttu-id="38f6d-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38f6d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f6d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38f6d-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f6d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f6d-136">CommonParameters</span></span>
<span data-ttu-id="38f6d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f6d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f6d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f6d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f6d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38f6d-139">INPUTS</span></span>

### <span data-ttu-id="38f6d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="38f6d-140">System.String</span></span>

## <span data-ttu-id="38f6d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38f6d-141">OUTPUTS</span></span>

### <span data-ttu-id="38f6d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38f6d-142">System.Boolean</span></span>

## <span data-ttu-id="38f6d-143">Note</span><span class="sxs-lookup"><span data-stu-id="38f6d-143">NOTES</span></span>

## <span data-ttu-id="38f6d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38f6d-144">RELATED LINKS</span></span>
