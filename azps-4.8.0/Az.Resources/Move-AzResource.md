---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 4f21ce7a14873d201fa18f45c96d508dcd38cb8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192635"
---
# <span data-ttu-id="7f96c-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-101">Move-AzResource</span></span>

## <span data-ttu-id="7f96c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f96c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f96c-103">Sposta una risorsa in un gruppo o un abbonamento di risorse diverso.</span><span class="sxs-lookup"><span data-stu-id="7f96c-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="7f96c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f96c-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f96c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f96c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f96c-106">Il cmdlet **Move-AzResource** sposta le risorse esistenti in un gruppo di risorse diverso.</span><span class="sxs-lookup"><span data-stu-id="7f96c-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="7f96c-107">Il gruppo di risorse può avere un abbonamento diverso.</span><span class="sxs-lookup"><span data-stu-id="7f96c-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="7f96c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f96c-108">EXAMPLES</span></span>

### <span data-ttu-id="7f96c-109">Esempio 1: trasferire una risorsa in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7f96c-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="7f96c-110">Con il primo comando viene ottenuta una risorsa denominata ContosoStorageAccount tramite il cmdlet Get-AzResource e la risorsa viene archiviata nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="7f96c-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="7f96c-111">Il secondo comando Sposta la risorsa nel gruppo di risorse denominato ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="7f96c-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="7f96c-112">Il comando identifica la risorsa per lo stato di trasferimento tramite la proprietà **resourceId** di $Resource.</span><span class="sxs-lookup"><span data-stu-id="7f96c-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="7f96c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f96c-113">PARAMETERS</span></span>

### <span data-ttu-id="7f96c-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f96c-114">-ApiVersion</span></span>
<span data-ttu-id="7f96c-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7f96c-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7f96c-116">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f96c-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7f96c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f96c-117">-DefaultProfile</span></span>
<span data-ttu-id="7f96c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f96c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f96c-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f96c-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="7f96c-120">Specifica il nome del gruppo di risorse in cui questo cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="7f96c-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="7f96c-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f96c-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="7f96c-122">Specifica l'ID della sottoscrizione in cui questo cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="7f96c-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="7f96c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7f96c-123">-Force</span></span>
<span data-ttu-id="7f96c-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7f96c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f96c-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="7f96c-125">-Pre</span></span>
<span data-ttu-id="7f96c-126">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7f96c-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7f96c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f96c-127">-ResourceId</span></span>
<span data-ttu-id="7f96c-128">Specifica una matrice di ID delle risorse spostate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f96c-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="7f96c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f96c-129">-Confirm</span></span>
<span data-ttu-id="7f96c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f96c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f96c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f96c-131">-WhatIf</span></span>
<span data-ttu-id="7f96c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f96c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f96c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f96c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f96c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f96c-134">CommonParameters</span></span>
<span data-ttu-id="7f96c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f96c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f96c-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f96c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f96c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f96c-137">INPUTS</span></span>

### <span data-ttu-id="7f96c-138">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f96c-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7f96c-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f96c-139">System.String[]</span></span>

## <span data-ttu-id="7f96c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f96c-140">OUTPUTS</span></span>

### <span data-ttu-id="7f96c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f96c-141">System.Boolean</span></span>

## <span data-ttu-id="7f96c-142">Note</span><span class="sxs-lookup"><span data-stu-id="7f96c-142">NOTES</span></span>

## <span data-ttu-id="7f96c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f96c-143">RELATED LINKS</span></span>

[<span data-ttu-id="7f96c-144">Trova-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-144">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="7f96c-145">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-145">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="7f96c-146">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-146">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="7f96c-147">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-147">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="7f96c-148">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="7f96c-148">Set-AzResource</span></span>](./Set-AzResource.md)


