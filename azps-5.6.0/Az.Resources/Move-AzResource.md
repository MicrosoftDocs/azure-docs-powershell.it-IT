---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962654"
---
# <span data-ttu-id="36f35-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="36f35-101">Move-AzResource</span></span>

## <span data-ttu-id="36f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f35-102">SYNOPSIS</span></span>
<span data-ttu-id="36f35-103">Sposta una risorsa in un gruppo di risorse o una sottoscrizione diversa.</span><span class="sxs-lookup"><span data-stu-id="36f35-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="36f35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36f35-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f35-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36f35-105">DESCRIPTION</span></span>
<span data-ttu-id="36f35-106">Il **cmdlet Move-AzResource** sposta le risorse esistenti in un gruppo di risorse diverso.</span><span class="sxs-lookup"><span data-stu-id="36f35-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="36f35-107">Il gruppo di risorse può essere in una sottoscrizione diversa.</span><span class="sxs-lookup"><span data-stu-id="36f35-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="36f35-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36f35-108">EXAMPLES</span></span>

### <span data-ttu-id="36f35-109">Esempio 1: Spostare una risorsa in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="36f35-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="36f35-110">Il primo comando ottiene una risorsa denominata ContosoStorageAccount usando il cmdlet Get-AzResource e quindi la archivia nella $Resource variabile.</span><span class="sxs-lookup"><span data-stu-id="36f35-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="36f35-111">Il secondo comando sposta la risorsa nel gruppo di risorse denominato Gruppo Risorse14.</span><span class="sxs-lookup"><span data-stu-id="36f35-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="36f35-112">Il comando identifica la risorsa da spostare usando la **proprietà ResourceId** di $Resource.</span><span class="sxs-lookup"><span data-stu-id="36f35-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="36f35-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36f35-113">PARAMETERS</span></span>

### <span data-ttu-id="36f35-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36f35-114">-ApiVersion</span></span>
<span data-ttu-id="36f35-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="36f35-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="36f35-116">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="36f35-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="36f35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f35-117">-DefaultProfile</span></span>
<span data-ttu-id="36f35-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="36f35-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f35-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="36f35-120">Specifica il nome del gruppo di risorse in cui il cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="36f35-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36f35-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="36f35-122">Specifica l'ID della sottoscrizione in cui questo cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="36f35-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-123">-Force</span><span class="sxs-lookup"><span data-stu-id="36f35-123">-Force</span></span>
<span data-ttu-id="36f35-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="36f35-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36f35-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="36f35-125">-Pre</span></span>
<span data-ttu-id="36f35-126">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="36f35-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36f35-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36f35-127">-ResourceId</span></span>
<span data-ttu-id="36f35-128">Specifica una matrice di ID delle risorse che il cmdlet sposta.</span><span class="sxs-lookup"><span data-stu-id="36f35-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36f35-129">-Confirm</span></span>
<span data-ttu-id="36f35-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f35-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f35-131">-WhatIf</span></span>
<span data-ttu-id="36f35-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36f35-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f35-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36f35-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f35-134">CommonParameters</span></span>
<span data-ttu-id="36f35-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f35-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36f35-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f35-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="36f35-137">INPUTS</span></span>

### <span data-ttu-id="36f35-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36f35-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36f35-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="36f35-139">System.String[]</span></span>

## <span data-ttu-id="36f35-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36f35-140">OUTPUTS</span></span>

### <span data-ttu-id="36f35-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36f35-141">System.Boolean</span></span>

## <span data-ttu-id="36f35-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="36f35-142">NOTES</span></span>

## <span data-ttu-id="36f35-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36f35-143">RELATED LINKS</span></span>

[<span data-ttu-id="36f35-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="36f35-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="36f35-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="36f35-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="36f35-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="36f35-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="36f35-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="36f35-147">Set-AzResource</span></span>](./Set-AzResource.md)


