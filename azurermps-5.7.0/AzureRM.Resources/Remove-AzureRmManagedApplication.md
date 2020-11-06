---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 1b5288b2ce0e453221819e6a0b80e06b45245160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509648"
---
# <span data-ttu-id="68045-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="68045-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="68045-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68045-102">SYNOPSIS</span></span>
<span data-ttu-id="68045-103">Rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="68045-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68045-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68045-104">SYNTAX</span></span>

### <span data-ttu-id="68045-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68045-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68045-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="68045-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68045-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68045-107">DESCRIPTION</span></span>
<span data-ttu-id="68045-108">Il cmdlet **Remove-AzureRmManagedApplication** rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="68045-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="68045-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68045-109">EXAMPLES</span></span>

### <span data-ttu-id="68045-110">Esempio 1: rimuovere l'applicazione gestita dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="68045-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="68045-111">Il primo comando ottiene un'applicazione gestita denominata myApp tramite il cmdlet Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="68045-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="68045-112">Il comando lo archivia nella variabile $Application.</span><span class="sxs-lookup"><span data-stu-id="68045-112">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="68045-113">Il secondo comando rimuove l'applicazione gestita identificata dalla proprietà **resourceId** di $Application.</span><span class="sxs-lookup"><span data-stu-id="68045-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="68045-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68045-114">PARAMETERS</span></span>

### <span data-ttu-id="68045-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68045-115">-ApiVersion</span></span>
<span data-ttu-id="68045-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="68045-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="68045-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="68045-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="68045-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68045-118">-DefaultProfile</span></span>
<span data-ttu-id="68045-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68045-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68045-120">-Force</span><span class="sxs-lookup"><span data-stu-id="68045-120">-Force</span></span>
<span data-ttu-id="68045-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="68045-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68045-122">-ID</span><span class="sxs-lookup"><span data-stu-id="68045-122">-Id</span></span>
<span data-ttu-id="68045-123">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="68045-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="68045-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="68045-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="68045-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="68045-125">-Name</span></span>
<span data-ttu-id="68045-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="68045-126">The managed application name.</span></span>

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

### <span data-ttu-id="68045-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="68045-127">-Pre</span></span>
<span data-ttu-id="68045-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="68045-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="68045-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68045-129">-ResourceGroupName</span></span>
<span data-ttu-id="68045-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68045-130">The resource group name.</span></span>

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

### <span data-ttu-id="68045-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68045-131">-Confirm</span></span>
<span data-ttu-id="68045-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68045-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68045-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68045-133">-WhatIf</span></span>
<span data-ttu-id="68045-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68045-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68045-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68045-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68045-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68045-136">CommonParameters</span></span>
<span data-ttu-id="68045-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68045-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68045-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68045-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68045-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68045-139">INPUTS</span></span>

### <span data-ttu-id="68045-140">System. String</span><span class="sxs-lookup"><span data-stu-id="68045-140">System.String</span></span>

## <span data-ttu-id="68045-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68045-141">OUTPUTS</span></span>

### <span data-ttu-id="68045-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68045-142">System.Boolean</span></span>

## <span data-ttu-id="68045-143">Note</span><span class="sxs-lookup"><span data-stu-id="68045-143">NOTES</span></span>

## <span data-ttu-id="68045-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68045-144">RELATED LINKS</span></span>
