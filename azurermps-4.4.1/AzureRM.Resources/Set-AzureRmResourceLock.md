---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687085"
---
# <span data-ttu-id="a1a3c-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a1a3c-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="a1a3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a3c-103">Modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1a3c-104">SYNTAX</span></span>

### <span data-ttu-id="a1a3c-105">Un blocco nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-105">A lock at the specified scope.</span></span> <span data-ttu-id="a1a3c-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="a1a3c-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-107">Un blocco nell'ambito del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-108">Un blocco nell'ambito delle risorse del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-109">Un blocco nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-110">Un blocco nell'ambito delle risorse dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-111">Un blocco nell'ambito delle risorse del tenant.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a3c-112">Un blocco, per ID.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a3c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1a3c-113">DESCRIPTION</span></span>
<span data-ttu-id="a1a3c-114">Il cmdlet **set-AzureRmResourceLock** modifica un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="a1a3c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1a3c-115">EXAMPLES</span></span>

### <span data-ttu-id="a1a3c-116">Esempio 1: aggiornare le note per un blocco</span><span class="sxs-lookup"><span data-stu-id="a1a3c-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a1a3c-117">Questo comando Aggiorna la nota per un blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="a1a3c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1a3c-118">PARAMETERS</span></span>

### <span data-ttu-id="a1a3c-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a1a3c-119">-ApiVersion</span></span>
<span data-ttu-id="a1a3c-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a1a3c-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a1a3c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a1a3c-122">-Force</span></span>
<span data-ttu-id="a1a3c-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1a3c-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a1a3c-124">-InformationAction</span></span>
<span data-ttu-id="a1a3c-125">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a1a3c-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1a3c-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1a3c-127">Continuare</span><span class="sxs-lookup"><span data-stu-id="a1a3c-127">Continue</span></span>
- <span data-ttu-id="a1a3c-128">Ignora</span><span class="sxs-lookup"><span data-stu-id="a1a3c-128">Ignore</span></span>
- <span data-ttu-id="a1a3c-129">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a1a3c-129">Inquire</span></span>
- <span data-ttu-id="a1a3c-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a1a3c-130">SilentlyContinue</span></span>
- <span data-ttu-id="a1a3c-131">Stop</span><span class="sxs-lookup"><span data-stu-id="a1a3c-131">Stop</span></span>
- <span data-ttu-id="a1a3c-132">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a1a3c-132">Suspend</span></span>

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

### <span data-ttu-id="a1a3c-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a1a3c-133">-InformationVariable</span></span>
<span data-ttu-id="a1a3c-134">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a1a3c-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="a1a3c-135">-LockId</span></span>
<span data-ttu-id="a1a3c-136">Specifica l'ID del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a1a3c-137">-LockLevel</span></span>
<span data-ttu-id="a1a3c-138">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="a1a3c-139">Attualmente, l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="a1a3c-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="a1a3c-140">-LockName</span></span>
<span data-ttu-id="a1a3c-141">Specifica il nome del blocco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="a1a3c-142">-LockNotes</span></span>
<span data-ttu-id="a1a3c-143">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="a1a3c-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1a3c-144">-Pre</span></span>
<span data-ttu-id="a1a3c-145">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1a3c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a3c-146">-ResourceGroupName</span></span>
<span data-ttu-id="a1a3c-147">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a1a3c-148">-ResourceName</span></span>
<span data-ttu-id="a1a3c-149">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a1a3c-150">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a1a3c-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a1a3c-151">`/`Database server</span><span class="sxs-lookup"><span data-stu-id="a1a3c-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a1a3c-152">-ResourceType</span></span>
<span data-ttu-id="a1a3c-153">Specifica il tipo di risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-154">-Ambito</span><span class="sxs-lookup"><span data-stu-id="a1a3c-154">-Scope</span></span>
<span data-ttu-id="a1a3c-155">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a1a3c-156">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a1a3c-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a1a3c-157">`/subscriptions/`nome del database del nome del gruppo di risorse ID abbonamento nome `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/`</span><span class="sxs-lookup"><span data-stu-id="a1a3c-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="a1a3c-158">Per specificare un gruppo di risorse, usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a1a3c-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="a1a3c-159">`/subscriptions/`nome del `/resourceGroups/` gruppo di risorse ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="a1a3c-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a1a3c-160">-TenantLevel</span></span>
<span data-ttu-id="a1a3c-161">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a3c-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1a3c-162">-Confirm</span></span>
<span data-ttu-id="a1a3c-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a3c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a3c-164">-WhatIf</span></span>
<span data-ttu-id="a1a3c-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a3c-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a3c-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a3c-167">-DefaultProfile</span></span>
<span data-ttu-id="a1a3c-168">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a3c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a3c-169">CommonParameters</span></span>
<span data-ttu-id="a1a3c-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a3c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a3c-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a3c-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a3c-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1a3c-172">INPUTS</span></span>

## <span data-ttu-id="a1a3c-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1a3c-173">OUTPUTS</span></span>

### <span data-ttu-id="a1a3c-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a1a3c-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a1a3c-175">Note</span><span class="sxs-lookup"><span data-stu-id="a1a3c-175">NOTES</span></span>

## <span data-ttu-id="a1a3c-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1a3c-176">RELATED LINKS</span></span>

[<span data-ttu-id="a1a3c-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a1a3c-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a1a3c-178">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a1a3c-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="a1a3c-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a1a3c-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

