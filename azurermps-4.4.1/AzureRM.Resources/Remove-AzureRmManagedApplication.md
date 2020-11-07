---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687706"
---
# <span data-ttu-id="26d8d-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="26d8d-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="26d8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="26d8d-103">Rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="26d8d-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26d8d-104">SYNTAX</span></span>

### <span data-ttu-id="26d8d-105">Set di parametri del nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="26d8d-105">The managed application name parameter set.</span></span> <span data-ttu-id="26d8d-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="26d8d-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8d-107">Set di parametri ID applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="26d8d-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26d8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26d8d-108">DESCRIPTION</span></span>
<span data-ttu-id="26d8d-109">Il cmdlet **Remove-AzureRmManagedApplication** rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="26d8d-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="26d8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26d8d-110">EXAMPLES</span></span>

### <span data-ttu-id="26d8d-111">Esempio 1: rimuovere l'applicazione gestita dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="26d8d-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="26d8d-112">Il primo comando ottiene un'applicazione gestita denominata myApp tramite il cmdlet Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="26d8d-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="26d8d-113">Il comando lo archivia nella variabile $Application.</span><span class="sxs-lookup"><span data-stu-id="26d8d-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="26d8d-114">Il secondo comando rimuove l'applicazione gestita identificata dalla proprietà **resourceId** di $Application.</span><span class="sxs-lookup"><span data-stu-id="26d8d-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="26d8d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26d8d-115">PARAMETERS</span></span>

### <span data-ttu-id="26d8d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26d8d-116">-ApiVersion</span></span>
<span data-ttu-id="26d8d-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="26d8d-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="26d8d-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="26d8d-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="26d8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d8d-119">-DefaultProfile</span></span>
<span data-ttu-id="26d8d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26d8d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26d8d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="26d8d-121">-Force</span></span>
<span data-ttu-id="26d8d-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="26d8d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="26d8d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="26d8d-123">-Id</span></span>
<span data-ttu-id="26d8d-124">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="26d8d-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="26d8d-125">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="26d8d-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26d8d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="26d8d-126">-Name</span></span>
<span data-ttu-id="26d8d-127">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="26d8d-127">The managed application name.</span></span>

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

### <span data-ttu-id="26d8d-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="26d8d-128">-Pre</span></span>
<span data-ttu-id="26d8d-129">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="26d8d-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="26d8d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26d8d-130">-ResourceGroupName</span></span>
<span data-ttu-id="26d8d-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26d8d-131">The resource group name.</span></span>

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

### <span data-ttu-id="26d8d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26d8d-132">-Confirm</span></span>
<span data-ttu-id="26d8d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26d8d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d8d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d8d-134">-WhatIf</span></span>
<span data-ttu-id="26d8d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26d8d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d8d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26d8d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d8d-137">CommonParameters</span></span>
<span data-ttu-id="26d8d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d8d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26d8d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d8d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26d8d-140">INPUTS</span></span>

### <span data-ttu-id="26d8d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="26d8d-141">System.String</span></span>

## <span data-ttu-id="26d8d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26d8d-142">OUTPUTS</span></span>

### <span data-ttu-id="26d8d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26d8d-143">System.Boolean</span></span>

## <span data-ttu-id="26d8d-144">Note</span><span class="sxs-lookup"><span data-stu-id="26d8d-144">NOTES</span></span>

## <span data-ttu-id="26d8d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26d8d-145">RELATED LINKS</span></span>

