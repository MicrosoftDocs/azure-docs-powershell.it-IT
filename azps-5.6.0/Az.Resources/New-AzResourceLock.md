---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 630ea593304523572403fce0db3d6118be66403f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970365"
---
# <span data-ttu-id="7d1ff-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7d1ff-101">New-AzResourceLock</span></span>

## <span data-ttu-id="7d1ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1ff-103">Crea un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-103">Creates a resource lock.</span></span>

## <span data-ttu-id="7d1ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d1ff-104">SYNTAX</span></span>

### <span data-ttu-id="7d1ff-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d1ff-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1ff-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d1ff-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ff-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="7d1ff-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ff-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="7d1ff-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1ff-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7d1ff-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ff-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="7d1ff-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d1ff-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d1ff-111">DESCRIPTION</span></span>
<span data-ttu-id="7d1ff-112">Il cmdlet **New-AzResourceLock** crea un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="7d1ff-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d1ff-113">EXAMPLES</span></span>

### <span data-ttu-id="7d1ff-114">Esempio 1: Creare un blocco di risorse in un sito Web</span><span class="sxs-lookup"><span data-stu-id="7d1ff-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="7d1ff-115">Questo comando crea un blocco di risorse su un sito Web.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="7d1ff-116">Esempio 2: Creare un blocco di risorse su un database</span><span class="sxs-lookup"><span data-stu-id="7d1ff-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="7d1ff-117">Questo comando crea un blocco delle risorse in un database di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="7d1ff-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d1ff-118">PARAMETERS</span></span>

### <span data-ttu-id="7d1ff-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d1ff-119">-ApiVersion</span></span>
<span data-ttu-id="7d1ff-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7d1ff-121">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7d1ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1ff-122">-DefaultProfile</span></span>
<span data-ttu-id="7d1ff-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d1ff-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1ff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7d1ff-124">-Force</span></span>
<span data-ttu-id="7d1ff-125">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d1ff-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="7d1ff-126">-LockId</span></span>
<span data-ttu-id="7d1ff-127">Specifica l'ID del blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-127">Specifies the ID of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="7d1ff-128">-LockLevel</span></span>
<span data-ttu-id="7d1ff-129">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="7d1ff-130">Attualmente, i valori validi sono CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="7d1ff-131">-LockName</span></span>
<span data-ttu-id="7d1ff-132">Specifica il nome del blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-132">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="7d1ff-133">-LockNotes</span></span>
<span data-ttu-id="7d1ff-134">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-134">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d1ff-135">-Pre</span></span>
<span data-ttu-id="7d1ff-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7d1ff-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1ff-137">-ResourceGroupName</span></span>
<span data-ttu-id="7d1ff-138">Specifica il nome di un gruppo di risorse per cui si applica il blocco o che contiene il gruppo di risorse a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7d1ff-139">-ResourceName</span></span>
<span data-ttu-id="7d1ff-140">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="7d1ff-141">Ad esempio, per specificare un database, usare il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7d1ff-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7d1ff-142">-ResourceType</span></span>
<span data-ttu-id="7d1ff-143">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-143">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-144">-Scope</span><span class="sxs-lookup"><span data-stu-id="7d1ff-144">-Scope</span></span>
<span data-ttu-id="7d1ff-145">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="7d1ff-146">Ad esempio, per specificare un database, usare il formato seguente: ID sottoscrizione ID gruppo di risorse Nome server nome database Per specificare un gruppo di risorse, usare il `/subscriptions/` `/resourceGroups/` formato `/providers/Microsoft.Sql/servers/` `/databases/` seguente: `/subscriptions/` NOME `/resourceGroups/` gruppo di risorse ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="7d1ff-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1ff-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d1ff-147">-Confirm</span></span>
<span data-ttu-id="7d1ff-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1ff-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1ff-149">-WhatIf</span></span>
<span data-ttu-id="7d1ff-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1ff-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1ff-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1ff-152">CommonParameters</span></span>
<span data-ttu-id="7d1ff-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1ff-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1ff-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d1ff-155">INPUTS</span></span>

### <span data-ttu-id="7d1ff-156">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1ff-156">System.String</span></span>

### <span data-ttu-id="7d1ff-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="7d1ff-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="7d1ff-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d1ff-158">OUTPUTS</span></span>

### <span data-ttu-id="7d1ff-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7d1ff-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7d1ff-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d1ff-160">NOTES</span></span>

## <span data-ttu-id="7d1ff-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d1ff-161">RELATED LINKS</span></span>

[<span data-ttu-id="7d1ff-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7d1ff-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="7d1ff-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7d1ff-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="7d1ff-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7d1ff-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


