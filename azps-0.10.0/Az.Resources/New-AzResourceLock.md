---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8d4f4180cc827c879dde0252044d30d5242d2300
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862477"
---
# <span data-ttu-id="6b298-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6b298-101">New-AzResourceLock</span></span>

## <span data-ttu-id="6b298-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b298-102">SYNOPSIS</span></span>
<span data-ttu-id="6b298-103">Crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b298-103">Creates a resource lock.</span></span>

## <span data-ttu-id="6b298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b298-104">SYNTAX</span></span>

### <span data-ttu-id="6b298-105">BySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b298-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b298-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b298-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b298-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="6b298-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b298-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="6b298-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b298-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6b298-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b298-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6b298-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b298-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="6b298-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b298-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b298-112">DESCRIPTION</span></span>
<span data-ttu-id="6b298-113">Il cmdlet **New-AzResourceLock** crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b298-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="6b298-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b298-114">EXAMPLES</span></span>

### <span data-ttu-id="6b298-115">Esempio 1: creare un blocco delle risorse in un sito Web</span><span class="sxs-lookup"><span data-stu-id="6b298-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="6b298-116">Questo comando crea un blocco delle risorse in un sito Web.</span><span class="sxs-lookup"><span data-stu-id="6b298-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="6b298-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b298-117">PARAMETERS</span></span>

### <span data-ttu-id="6b298-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b298-118">-ApiVersion</span></span>
<span data-ttu-id="6b298-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="6b298-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6b298-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b298-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6b298-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b298-121">-DefaultProfile</span></span>
<span data-ttu-id="6b298-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6b298-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b298-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6b298-123">-Force</span></span>
<span data-ttu-id="6b298-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6b298-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b298-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b298-125">-InformationAction</span></span>
<span data-ttu-id="6b298-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6b298-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="6b298-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b298-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b298-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="6b298-128">Continue</span></span>
- <span data-ttu-id="6b298-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="6b298-129">Ignore</span></span>
- <span data-ttu-id="6b298-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6b298-130">Inquire</span></span>
- <span data-ttu-id="6b298-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b298-131">SilentlyContinue</span></span>
- <span data-ttu-id="6b298-132">Stop</span><span class="sxs-lookup"><span data-stu-id="6b298-132">Stop</span></span>
- <span data-ttu-id="6b298-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6b298-133">Suspend</span></span>

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

### <span data-ttu-id="6b298-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b298-134">-InformationVariable</span></span>
<span data-ttu-id="6b298-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b298-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b298-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="6b298-136">-LockId</span></span>
<span data-ttu-id="6b298-137">Specifica l'ID del blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="6b298-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="6b298-138">-LockLevel</span></span>
<span data-ttu-id="6b298-139">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="6b298-140">Attualmente i valori validi sono CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6b298-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="6b298-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="6b298-141">-LockName</span></span>
<span data-ttu-id="6b298-142">Specifica il nome del blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="6b298-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="6b298-143">-LockNotes</span></span>
<span data-ttu-id="6b298-144">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="6b298-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b298-145">-Pre</span></span>
<span data-ttu-id="6b298-146">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6b298-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6b298-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b298-147">-ResourceGroupName</span></span>
<span data-ttu-id="6b298-148">Specifica il nome di un gruppo di risorse per cui si applica il blocco o che contiene il gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="6b298-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b298-149">-ResourceName</span></span>
<span data-ttu-id="6b298-150">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="6b298-151">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6b298-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6b298-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6b298-152">-ResourceType</span></span>
<span data-ttu-id="6b298-153">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="6b298-154">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6b298-154">-Scope</span></span>
<span data-ttu-id="6b298-155">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="6b298-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="6b298-156">Ad esempio, per specificare un database, usare il formato seguente: nome del gruppo di risorse ID abbonamento nome del nome del `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/` di database per specificare un gruppo di risorse, usare il formato seguente: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="6b298-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="6b298-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6b298-157">-TenantLevel</span></span>
<span data-ttu-id="6b298-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="6b298-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6b298-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b298-159">-Confirm</span></span>
<span data-ttu-id="6b298-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b298-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b298-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b298-161">-WhatIf</span></span>
<span data-ttu-id="6b298-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b298-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b298-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b298-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b298-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b298-164">CommonParameters</span></span>
<span data-ttu-id="6b298-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b298-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b298-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b298-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b298-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b298-167">INPUTS</span></span>

## <span data-ttu-id="6b298-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b298-168">OUTPUTS</span></span>

## <span data-ttu-id="6b298-169">Note</span><span class="sxs-lookup"><span data-stu-id="6b298-169">NOTES</span></span>

## <span data-ttu-id="6b298-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b298-170">RELATED LINKS</span></span>

[<span data-ttu-id="6b298-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6b298-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="6b298-172">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6b298-172">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="6b298-173">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6b298-173">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


