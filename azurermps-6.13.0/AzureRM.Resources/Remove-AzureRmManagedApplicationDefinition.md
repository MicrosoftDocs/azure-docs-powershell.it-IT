---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: d8257c2f6d37ebd6c304fd511e889d8314fd0266
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514828"
---
# <span data-ttu-id="733b7-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="733b7-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="733b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="733b7-102">SYNOPSIS</span></span>
<span data-ttu-id="733b7-103">Rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="733b7-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="733b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="733b7-104">SYNTAX</span></span>

### <span data-ttu-id="733b7-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="733b7-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="733b7-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="733b7-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="733b7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="733b7-107">DESCRIPTION</span></span>
<span data-ttu-id="733b7-108">Il cmdlet **Remove-AzureRmManagedApplicationDefinition** rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="733b7-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="733b7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="733b7-109">EXAMPLES</span></span>

### <span data-ttu-id="733b7-110">Esempio 1: rimuovere la definizione di applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="733b7-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="733b7-111">Il primo comando ottiene una definizione di applicazione gestita denominata myAppDef tramite il cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="733b7-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="733b7-112">Il comando lo archivia nella variabile $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="733b7-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="733b7-113">Il secondo comando rimuove la definizione dell'applicazione gestita identificata dalla proprietà **resourceId** di $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="733b7-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="733b7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="733b7-114">PARAMETERS</span></span>

### <span data-ttu-id="733b7-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="733b7-115">-ApiVersion</span></span>
<span data-ttu-id="733b7-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="733b7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="733b7-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="733b7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="733b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733b7-118">-DefaultProfile</span></span>
<span data-ttu-id="733b7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="733b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="733b7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="733b7-120">-Force</span></span>
<span data-ttu-id="733b7-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="733b7-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="733b7-122">-ID</span><span class="sxs-lookup"><span data-stu-id="733b7-122">-Id</span></span>
<span data-ttu-id="733b7-123">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="733b7-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="733b7-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="733b7-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="733b7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="733b7-125">-Name</span></span>
<span data-ttu-id="733b7-126">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="733b7-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="733b7-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="733b7-127">-Pre</span></span>
<span data-ttu-id="733b7-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="733b7-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="733b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="733b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="733b7-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="733b7-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="733b7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="733b7-131">-Confirm</span></span>
<span data-ttu-id="733b7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="733b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="733b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="733b7-133">-WhatIf</span></span>
<span data-ttu-id="733b7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="733b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="733b7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="733b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="733b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733b7-136">CommonParameters</span></span>
<span data-ttu-id="733b7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="733b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733b7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733b7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733b7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="733b7-139">INPUTS</span></span>

### <span data-ttu-id="733b7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="733b7-140">System.String</span></span>

## <span data-ttu-id="733b7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="733b7-141">OUTPUTS</span></span>

### <span data-ttu-id="733b7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="733b7-142">System.Boolean</span></span>

## <span data-ttu-id="733b7-143">Note</span><span class="sxs-lookup"><span data-stu-id="733b7-143">NOTES</span></span>

## <span data-ttu-id="733b7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="733b7-144">RELATED LINKS</span></span>
