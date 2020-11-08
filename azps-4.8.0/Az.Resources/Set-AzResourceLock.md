---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188884"
---
# <span data-ttu-id="06819-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="06819-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="06819-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06819-102">SYNOPSIS</span></span>
<span data-ttu-id="06819-103">Modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="06819-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="06819-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06819-104">SYNTAX</span></span>

### <span data-ttu-id="06819-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06819-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06819-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06819-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06819-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="06819-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06819-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="06819-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06819-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="06819-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06819-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="06819-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06819-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06819-111">DESCRIPTION</span></span>
<span data-ttu-id="06819-112">Il cmdlet **set-AzResourceLock** modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="06819-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="06819-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06819-113">EXAMPLES</span></span>

### <span data-ttu-id="06819-114">Esempio 1: aggiornare le note per un blocco</span><span class="sxs-lookup"><span data-stu-id="06819-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="06819-115">Questo comando Aggiorna la nota per un blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="06819-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="06819-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06819-116">PARAMETERS</span></span>

### <span data-ttu-id="06819-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06819-117">-ApiVersion</span></span>
<span data-ttu-id="06819-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="06819-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="06819-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="06819-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="06819-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06819-120">-DefaultProfile</span></span>
<span data-ttu-id="06819-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="06819-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06819-122">-Force</span><span class="sxs-lookup"><span data-stu-id="06819-122">-Force</span></span>
<span data-ttu-id="06819-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06819-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06819-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="06819-124">-LockId</span></span>
<span data-ttu-id="06819-125">Specifica l'ID del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06819-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="06819-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="06819-126">-LockLevel</span></span>
<span data-ttu-id="06819-127">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="06819-128">Attualmente, l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="06819-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="06819-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="06819-129">-LockName</span></span>
<span data-ttu-id="06819-130">Specifica il nome del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06819-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="06819-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="06819-131">-LockNotes</span></span>
<span data-ttu-id="06819-132">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="06819-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="06819-133">-Pre</span></span>
<span data-ttu-id="06819-134">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="06819-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="06819-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06819-135">-ResourceGroupName</span></span>
<span data-ttu-id="06819-136">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="06819-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06819-137">-ResourceName</span></span>
<span data-ttu-id="06819-138">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="06819-139">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="06819-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="06819-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="06819-140">-ResourceType</span></span>
<span data-ttu-id="06819-141">Specifica il tipo di risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="06819-142">-Ambito</span><span class="sxs-lookup"><span data-stu-id="06819-142">-Scope</span></span>
<span data-ttu-id="06819-143">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="06819-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="06819-144">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="06819-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="06819-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06819-145">-Confirm</span></span>
<span data-ttu-id="06819-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06819-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06819-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06819-147">-WhatIf</span></span>
<span data-ttu-id="06819-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06819-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06819-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06819-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06819-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06819-150">CommonParameters</span></span>
<span data-ttu-id="06819-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06819-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06819-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06819-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06819-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06819-153">INPUTS</span></span>

### <span data-ttu-id="06819-154">System. String</span><span class="sxs-lookup"><span data-stu-id="06819-154">System.String</span></span>

### <span data-ttu-id="06819-155">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="06819-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="06819-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06819-156">OUTPUTS</span></span>

### <span data-ttu-id="06819-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06819-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06819-158">Note</span><span class="sxs-lookup"><span data-stu-id="06819-158">NOTES</span></span>

## <span data-ttu-id="06819-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06819-159">RELATED LINKS</span></span>

[<span data-ttu-id="06819-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="06819-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="06819-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="06819-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="06819-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="06819-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

