---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 8556f71263aefe721225906aa1480c4f0bc19f7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866810"
---
# <span data-ttu-id="156ce-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="156ce-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="156ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="156ce-102">SYNOPSIS</span></span>
<span data-ttu-id="156ce-103">Crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="156ce-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="156ce-104">SYNTAX</span></span>

### <span data-ttu-id="156ce-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="156ce-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="156ce-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="156ce-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="156ce-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="156ce-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156ce-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="156ce-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="156ce-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="156ce-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156ce-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="156ce-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156ce-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="156ce-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="156ce-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="156ce-112">DESCRIPTION</span></span>
<span data-ttu-id="156ce-113">Il cmdlet **New-AzureRmResourceLock** crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="156ce-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="156ce-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="156ce-114">EXAMPLES</span></span>

### <span data-ttu-id="156ce-115">Esempio 1: creare un blocco delle risorse in un sito Web</span><span class="sxs-lookup"><span data-stu-id="156ce-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="156ce-116">Questo comando crea un blocco delle risorse in un sito Web.</span><span class="sxs-lookup"><span data-stu-id="156ce-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="156ce-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="156ce-117">PARAMETERS</span></span>

### <span data-ttu-id="156ce-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="156ce-118">-ApiVersion</span></span>
<span data-ttu-id="156ce-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="156ce-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="156ce-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="156ce-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="156ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156ce-121">-DefaultProfile</span></span>
<span data-ttu-id="156ce-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="156ce-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="156ce-123">-Force</span><span class="sxs-lookup"><span data-stu-id="156ce-123">-Force</span></span>
<span data-ttu-id="156ce-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="156ce-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="156ce-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="156ce-125">-InformationAction</span></span>
<span data-ttu-id="156ce-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="156ce-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="156ce-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="156ce-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="156ce-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="156ce-128">Continue</span></span>
- <span data-ttu-id="156ce-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="156ce-129">Ignore</span></span>
- <span data-ttu-id="156ce-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="156ce-130">Inquire</span></span>
- <span data-ttu-id="156ce-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="156ce-131">SilentlyContinue</span></span>
- <span data-ttu-id="156ce-132">Stop</span><span class="sxs-lookup"><span data-stu-id="156ce-132">Stop</span></span>
- <span data-ttu-id="156ce-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="156ce-133">Suspend</span></span>

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

### <span data-ttu-id="156ce-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="156ce-134">-InformationVariable</span></span>
<span data-ttu-id="156ce-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="156ce-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="156ce-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="156ce-136">-LockId</span></span>
<span data-ttu-id="156ce-137">Specifica l'ID del blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="156ce-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="156ce-138">-LockLevel</span></span>
<span data-ttu-id="156ce-139">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="156ce-140">Attualmente i valori validi sono CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="156ce-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="156ce-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="156ce-141">-LockName</span></span>
<span data-ttu-id="156ce-142">Specifica il nome del blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="156ce-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="156ce-143">-LockNotes</span></span>
<span data-ttu-id="156ce-144">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="156ce-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="156ce-145">-Pre</span></span>
<span data-ttu-id="156ce-146">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="156ce-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="156ce-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156ce-147">-ResourceGroupName</span></span>
<span data-ttu-id="156ce-148">Specifica il nome di un gruppo di risorse per cui si applica il blocco o che contiene il gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="156ce-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="156ce-149">-ResourceName</span></span>
<span data-ttu-id="156ce-150">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="156ce-151">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="156ce-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="156ce-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="156ce-152">-ResourceType</span></span>
<span data-ttu-id="156ce-153">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="156ce-154">-Ambito</span><span class="sxs-lookup"><span data-stu-id="156ce-154">-Scope</span></span>
<span data-ttu-id="156ce-155">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="156ce-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="156ce-156">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="156ce-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="156ce-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="156ce-157">-TenantLevel</span></span>
<span data-ttu-id="156ce-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="156ce-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="156ce-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="156ce-159">-Confirm</span></span>
<span data-ttu-id="156ce-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="156ce-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156ce-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156ce-161">-WhatIf</span></span>
<span data-ttu-id="156ce-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="156ce-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156ce-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="156ce-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156ce-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ce-164">CommonParameters</span></span>
<span data-ttu-id="156ce-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156ce-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ce-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156ce-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ce-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="156ce-167">INPUTS</span></span>

## <span data-ttu-id="156ce-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="156ce-168">OUTPUTS</span></span>

## <span data-ttu-id="156ce-169">Note</span><span class="sxs-lookup"><span data-stu-id="156ce-169">NOTES</span></span>

## <span data-ttu-id="156ce-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="156ce-170">RELATED LINKS</span></span>

[<span data-ttu-id="156ce-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="156ce-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="156ce-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="156ce-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="156ce-173">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="156ce-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


