---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862334"
---
# <span data-ttu-id="77dbc-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77dbc-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="77dbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="77dbc-103">Modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="77dbc-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="77dbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77dbc-104">SYNTAX</span></span>

### <span data-ttu-id="77dbc-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77dbc-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77dbc-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77dbc-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77dbc-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="77dbc-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77dbc-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="77dbc-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77dbc-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="77dbc-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77dbc-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="77dbc-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77dbc-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="77dbc-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77dbc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77dbc-112">DESCRIPTION</span></span>
<span data-ttu-id="77dbc-113">Il cmdlet **set-AzResourceLock** modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="77dbc-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="77dbc-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77dbc-114">EXAMPLES</span></span>

### <span data-ttu-id="77dbc-115">Esempio 1: aggiornare le note per un blocco</span><span class="sxs-lookup"><span data-stu-id="77dbc-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="77dbc-116">Questo comando Aggiorna la nota per un blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="77dbc-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="77dbc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77dbc-117">PARAMETERS</span></span>

### <span data-ttu-id="77dbc-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="77dbc-118">-ApiVersion</span></span>
<span data-ttu-id="77dbc-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="77dbc-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="77dbc-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="77dbc-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="77dbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dbc-121">-DefaultProfile</span></span>
<span data-ttu-id="77dbc-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="77dbc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dbc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="77dbc-123">-Force</span></span>
<span data-ttu-id="77dbc-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77dbc-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77dbc-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="77dbc-125">-InformationAction</span></span>
<span data-ttu-id="77dbc-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="77dbc-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="77dbc-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77dbc-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77dbc-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="77dbc-128">Continue</span></span>
- <span data-ttu-id="77dbc-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="77dbc-129">Ignore</span></span>
- <span data-ttu-id="77dbc-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="77dbc-130">Inquire</span></span>
- <span data-ttu-id="77dbc-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77dbc-131">SilentlyContinue</span></span>
- <span data-ttu-id="77dbc-132">Stop</span><span class="sxs-lookup"><span data-stu-id="77dbc-132">Stop</span></span>
- <span data-ttu-id="77dbc-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="77dbc-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dbc-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77dbc-134">-InformationVariable</span></span>
<span data-ttu-id="77dbc-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="77dbc-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dbc-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="77dbc-136">-LockId</span></span>
<span data-ttu-id="77dbc-137">Specifica l'ID del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77dbc-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="77dbc-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="77dbc-138">-LockLevel</span></span>
<span data-ttu-id="77dbc-139">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="77dbc-140">Attualmente, l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="77dbc-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbc-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="77dbc-141">-LockName</span></span>
<span data-ttu-id="77dbc-142">Specifica il nome del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77dbc-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="77dbc-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="77dbc-143">-LockNotes</span></span>
<span data-ttu-id="77dbc-144">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="77dbc-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="77dbc-145">-Pre</span></span>
<span data-ttu-id="77dbc-146">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="77dbc-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="77dbc-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dbc-147">-ResourceGroupName</span></span>
<span data-ttu-id="77dbc-148">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="77dbc-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="77dbc-149">-ResourceName</span></span>
<span data-ttu-id="77dbc-150">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="77dbc-151">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="77dbc-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="77dbc-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="77dbc-152">-ResourceType</span></span>
<span data-ttu-id="77dbc-153">Specifica il tipo di risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="77dbc-154">-Ambito</span><span class="sxs-lookup"><span data-stu-id="77dbc-154">-Scope</span></span>
<span data-ttu-id="77dbc-155">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="77dbc-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="77dbc-156">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="77dbc-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="77dbc-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="77dbc-157">-TenantLevel</span></span>
<span data-ttu-id="77dbc-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="77dbc-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="77dbc-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77dbc-159">-Confirm</span></span>
<span data-ttu-id="77dbc-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77dbc-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77dbc-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dbc-161">-WhatIf</span></span>
<span data-ttu-id="77dbc-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77dbc-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dbc-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77dbc-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77dbc-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dbc-164">CommonParameters</span></span>
<span data-ttu-id="77dbc-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dbc-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dbc-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dbc-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dbc-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77dbc-167">INPUTS</span></span>

## <span data-ttu-id="77dbc-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77dbc-168">OUTPUTS</span></span>

## <span data-ttu-id="77dbc-169">Note</span><span class="sxs-lookup"><span data-stu-id="77dbc-169">NOTES</span></span>

## <span data-ttu-id="77dbc-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77dbc-170">RELATED LINKS</span></span>

[<span data-ttu-id="77dbc-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77dbc-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="77dbc-172">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77dbc-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="77dbc-173">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77dbc-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


