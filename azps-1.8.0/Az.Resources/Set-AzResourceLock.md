---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677265"
---
# <span data-ttu-id="1dca6-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1dca6-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="1dca6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dca6-102">SYNOPSIS</span></span>
<span data-ttu-id="1dca6-103">Modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dca6-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="1dca6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dca6-104">SYNTAX</span></span>

### <span data-ttu-id="1dca6-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dca6-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dca6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1dca6-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dca6-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dca6-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="1dca6-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dca6-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dca6-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dca6-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="1dca6-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dca6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dca6-112">DESCRIPTION</span></span>
<span data-ttu-id="1dca6-113">Il cmdlet **set-AzResourceLock** modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dca6-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="1dca6-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dca6-114">EXAMPLES</span></span>

### <span data-ttu-id="1dca6-115">Esempio 1: aggiornare le note per un blocco</span><span class="sxs-lookup"><span data-stu-id="1dca6-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1dca6-116">Questo comando Aggiorna la nota per un blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="1dca6-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="1dca6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dca6-117">PARAMETERS</span></span>

### <span data-ttu-id="1dca6-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1dca6-118">-ApiVersion</span></span>
<span data-ttu-id="1dca6-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1dca6-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1dca6-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="1dca6-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1dca6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dca6-121">-DefaultProfile</span></span>
<span data-ttu-id="1dca6-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1dca6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dca6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1dca6-123">-Force</span></span>
<span data-ttu-id="1dca6-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1dca6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dca6-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="1dca6-125">-LockId</span></span>
<span data-ttu-id="1dca6-126">Specifica l'ID del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dca6-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1dca6-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-127">-LockLevel</span></span>
<span data-ttu-id="1dca6-128">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="1dca6-129">Attualmente, l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="1dca6-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="1dca6-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="1dca6-130">-LockName</span></span>
<span data-ttu-id="1dca6-131">Specifica il nome del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dca6-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dca6-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="1dca6-132">-LockNotes</span></span>
<span data-ttu-id="1dca6-133">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="1dca6-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="1dca6-134">-Pre</span></span>
<span data-ttu-id="1dca6-135">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1dca6-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1dca6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dca6-136">-ResourceGroupName</span></span>
<span data-ttu-id="1dca6-137">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="1dca6-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1dca6-138">-ResourceName</span></span>
<span data-ttu-id="1dca6-139">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="1dca6-140">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="1dca6-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dca6-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1dca6-141">-ResourceType</span></span>
<span data-ttu-id="1dca6-142">Specifica il tipo di risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-142">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dca6-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1dca6-143">-Scope</span></span>
<span data-ttu-id="1dca6-144">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="1dca6-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="1dca6-145">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="1dca6-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="1dca6-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-146">-TenantLevel</span></span>
<span data-ttu-id="1dca6-147">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="1dca6-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dca6-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dca6-148">-Confirm</span></span>
<span data-ttu-id="1dca6-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dca6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dca6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dca6-150">-WhatIf</span></span>
<span data-ttu-id="1dca6-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dca6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dca6-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dca6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dca6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dca6-153">CommonParameters</span></span>
<span data-ttu-id="1dca6-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dca6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dca6-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dca6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dca6-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dca6-156">INPUTS</span></span>

### <span data-ttu-id="1dca6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1dca6-157">System.String</span></span>

### <span data-ttu-id="1dca6-158">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="1dca6-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="1dca6-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dca6-159">OUTPUTS</span></span>

### <span data-ttu-id="1dca6-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1dca6-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1dca6-161">Note</span><span class="sxs-lookup"><span data-stu-id="1dca6-161">NOTES</span></span>

## <span data-ttu-id="1dca6-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dca6-162">RELATED LINKS</span></span>

[<span data-ttu-id="1dca6-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1dca6-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="1dca6-164">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1dca6-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="1dca6-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1dca6-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

