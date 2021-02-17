---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178759"
---
# <span data-ttu-id="55809-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55809-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="55809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55809-102">SYNOPSIS</span></span>
<span data-ttu-id="55809-103">Modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="55809-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="55809-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55809-104">SYNTAX</span></span>

### <span data-ttu-id="55809-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55809-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55809-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55809-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55809-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="55809-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55809-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="55809-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55809-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="55809-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55809-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="55809-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55809-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55809-111">DESCRIPTION</span></span>
<span data-ttu-id="55809-112">Il cmdlet **Set-AzResourceLock** modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="55809-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="55809-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55809-113">EXAMPLES</span></span>

### <span data-ttu-id="55809-114">Esempio 1: Aggiornare le note per un blocco</span><span class="sxs-lookup"><span data-stu-id="55809-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="55809-115">Questo comando aggiorna la nota per un lucchetto denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="55809-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="55809-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55809-116">PARAMETERS</span></span>

### <span data-ttu-id="55809-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55809-117">-ApiVersion</span></span>
<span data-ttu-id="55809-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="55809-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="55809-119">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="55809-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="55809-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55809-120">-DefaultProfile</span></span>
<span data-ttu-id="55809-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="55809-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55809-122">-Force</span><span class="sxs-lookup"><span data-stu-id="55809-122">-Force</span></span>
<span data-ttu-id="55809-123">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="55809-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55809-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="55809-124">-LockId</span></span>
<span data-ttu-id="55809-125">Specifica l'ID del blocco modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55809-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="55809-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="55809-126">-LockLevel</span></span>
<span data-ttu-id="55809-127">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="55809-128">Attualmente l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="55809-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="55809-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="55809-129">-LockName</span></span>
<span data-ttu-id="55809-130">Specifica il nome del blocco modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55809-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="55809-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="55809-131">-LockNotes</span></span>
<span data-ttu-id="55809-132">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="55809-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="55809-133">-Pre</span></span>
<span data-ttu-id="55809-134">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="55809-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="55809-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55809-135">-ResourceGroupName</span></span>
<span data-ttu-id="55809-136">Specifica il nome del gruppo di risorse a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="55809-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="55809-137">-ResourceName</span></span>
<span data-ttu-id="55809-138">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="55809-139">Ad esempio, per specificare un database, usare il formato seguente: Database server `/`</span><span class="sxs-lookup"><span data-stu-id="55809-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="55809-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="55809-140">-ResourceType</span></span>
<span data-ttu-id="55809-141">Specifica il tipo di risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="55809-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="55809-142">-Scope</span></span>
<span data-ttu-id="55809-143">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="55809-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="55809-144">Ad esempio, per specificare un database, usare il formato seguente: ID sottoscrizione ID gruppo di risorse Nome server nome database Per specificare un gruppo di risorse, usare il `/subscriptions/` `/resourceGroups/` formato `/providers/Microsoft.Sql/servers/` `/databases/` seguente: `/subscriptions/` NOME `/resourceGroups/` gruppo di risorse ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="55809-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="55809-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55809-145">-Confirm</span></span>
<span data-ttu-id="55809-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55809-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55809-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55809-147">-WhatIf</span></span>
<span data-ttu-id="55809-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55809-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55809-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55809-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55809-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55809-150">CommonParameters</span></span>
<span data-ttu-id="55809-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55809-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55809-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="55809-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55809-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="55809-153">INPUTS</span></span>

### <span data-ttu-id="55809-154">System.String</span><span class="sxs-lookup"><span data-stu-id="55809-154">System.String</span></span>

### <span data-ttu-id="55809-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="55809-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="55809-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55809-156">OUTPUTS</span></span>

### <span data-ttu-id="55809-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="55809-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55809-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="55809-158">NOTES</span></span>

## <span data-ttu-id="55809-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55809-159">RELATED LINKS</span></span>

[<span data-ttu-id="55809-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55809-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="55809-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55809-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="55809-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="55809-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


