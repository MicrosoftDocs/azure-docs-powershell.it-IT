---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520768"
---
# <span data-ttu-id="a3965-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a3965-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="a3965-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3965-102">SYNOPSIS</span></span>
<span data-ttu-id="a3965-103">Rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="a3965-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3965-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3965-104">SYNTAX</span></span>

### <span data-ttu-id="a3965-105">Set di parametri del nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a3965-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="a3965-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="a3965-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3965-107">Set di parametri ID definizione applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a3965-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3965-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3965-108">DESCRIPTION</span></span>
<span data-ttu-id="a3965-109">Il cmdlet **Remove-AzureRmManagedApplicationDefinition** rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="a3965-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="a3965-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3965-110">EXAMPLES</span></span>

### <span data-ttu-id="a3965-111">Esempio 1: rimuovere la definizione di applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a3965-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="a3965-112">Il primo comando ottiene una definizione di applicazione gestita denominata myAppDef tramite il cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="a3965-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="a3965-113">Il comando lo archivia nella variabile $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="a3965-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="a3965-114">Il secondo comando rimuove la definizione dell'applicazione gestita identificata dalla proprietà **resourceId** di $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="a3965-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="a3965-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3965-115">PARAMETERS</span></span>

### <span data-ttu-id="a3965-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a3965-116">-ApiVersion</span></span>
<span data-ttu-id="a3965-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a3965-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a3965-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="a3965-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a3965-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3965-119">-DefaultProfile</span></span>
<span data-ttu-id="a3965-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3965-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3965-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a3965-121">-Force</span></span>
<span data-ttu-id="a3965-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a3965-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3965-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a3965-123">-Id</span></span>
<span data-ttu-id="a3965-124">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a3965-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="a3965-125">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a3965-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3965-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3965-126">-Name</span></span>
<span data-ttu-id="a3965-127">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a3965-127">The managed application definition name.</span></span>

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

### <span data-ttu-id="a3965-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="a3965-128">-Pre</span></span>
<span data-ttu-id="a3965-129">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a3965-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a3965-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3965-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3965-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3965-131">The resource group name.</span></span>

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

### <span data-ttu-id="a3965-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3965-132">-Confirm</span></span>
<span data-ttu-id="a3965-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3965-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3965-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3965-134">-WhatIf</span></span>
<span data-ttu-id="a3965-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3965-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3965-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3965-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3965-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3965-137">CommonParameters</span></span>
<span data-ttu-id="a3965-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3965-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3965-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3965-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3965-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3965-140">INPUTS</span></span>

### <span data-ttu-id="a3965-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a3965-141">System.String</span></span>

## <span data-ttu-id="a3965-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3965-142">OUTPUTS</span></span>

### <span data-ttu-id="a3965-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3965-143">System.Boolean</span></span>

## <span data-ttu-id="a3965-144">Note</span><span class="sxs-lookup"><span data-stu-id="a3965-144">NOTES</span></span>

## <span data-ttu-id="a3965-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3965-145">RELATED LINKS</span></span>

