---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8c4352f6345bc6de76208d6821aadd6c249174ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864625"
---
# <span data-ttu-id="20db2-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="20db2-101">New-AzResourceLock</span></span>

## <span data-ttu-id="20db2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20db2-102">SYNOPSIS</span></span>
<span data-ttu-id="20db2-103">Crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="20db2-103">Creates a resource lock.</span></span>

## <span data-ttu-id="20db2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20db2-104">SYNTAX</span></span>

### <span data-ttu-id="20db2-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20db2-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20db2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20db2-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20db2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20db2-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="20db2-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20db2-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20db2-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20db2-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="20db2-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20db2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20db2-112">DESCRIPTION</span></span>
<span data-ttu-id="20db2-113">Il cmdlet **New-AzResourceLock** crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="20db2-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="20db2-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20db2-114">EXAMPLES</span></span>

### <span data-ttu-id="20db2-115">Esempio 1: creare un blocco delle risorse in un sito Web</span><span class="sxs-lookup"><span data-stu-id="20db2-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="20db2-116">Questo comando crea un blocco delle risorse in un sito Web.</span><span class="sxs-lookup"><span data-stu-id="20db2-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="20db2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20db2-117">PARAMETERS</span></span>

### <span data-ttu-id="20db2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20db2-118">-ApiVersion</span></span>
<span data-ttu-id="20db2-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="20db2-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="20db2-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="20db2-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="20db2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20db2-121">-DefaultProfile</span></span>
<span data-ttu-id="20db2-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="20db2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20db2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="20db2-123">-Force</span></span>
<span data-ttu-id="20db2-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="20db2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20db2-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="20db2-125">-LockId</span></span>
<span data-ttu-id="20db2-126">Specifica l'ID del blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="20db2-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-127">-LockLevel</span></span>
<span data-ttu-id="20db2-128">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="20db2-129">Attualmente i valori validi sono CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="20db2-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="20db2-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="20db2-130">-LockName</span></span>
<span data-ttu-id="20db2-131">Specifica il nome del blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="20db2-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="20db2-132">-LockNotes</span></span>
<span data-ttu-id="20db2-133">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="20db2-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="20db2-134">-Pre</span></span>
<span data-ttu-id="20db2-135">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="20db2-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="20db2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20db2-136">-ResourceGroupName</span></span>
<span data-ttu-id="20db2-137">Specifica il nome di un gruppo di risorse per cui si applica il blocco o che contiene il gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="20db2-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="20db2-138">-ResourceName</span></span>
<span data-ttu-id="20db2-139">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="20db2-140">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="20db2-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="20db2-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="20db2-141">-ResourceType</span></span>
<span data-ttu-id="20db2-142">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="20db2-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="20db2-143">-Scope</span></span>
<span data-ttu-id="20db2-144">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="20db2-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="20db2-145">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="20db2-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="20db2-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-146">-TenantLevel</span></span>
<span data-ttu-id="20db2-147">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="20db2-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="20db2-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20db2-148">-Confirm</span></span>
<span data-ttu-id="20db2-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20db2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20db2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20db2-150">-WhatIf</span></span>
<span data-ttu-id="20db2-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20db2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20db2-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20db2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20db2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20db2-153">CommonParameters</span></span>
<span data-ttu-id="20db2-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20db2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20db2-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20db2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20db2-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20db2-156">INPUTS</span></span>

### <span data-ttu-id="20db2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="20db2-157">System.String</span></span>

### <span data-ttu-id="20db2-158">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="20db2-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="20db2-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20db2-159">OUTPUTS</span></span>

### <span data-ttu-id="20db2-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="20db2-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="20db2-161">Note</span><span class="sxs-lookup"><span data-stu-id="20db2-161">NOTES</span></span>

## <span data-ttu-id="20db2-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20db2-162">RELATED LINKS</span></span>

[<span data-ttu-id="20db2-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="20db2-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="20db2-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="20db2-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="20db2-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="20db2-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


