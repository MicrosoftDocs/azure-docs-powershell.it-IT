---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521537"
---
# <span data-ttu-id="320bd-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="320bd-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="320bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="320bd-102">SYNOPSIS</span></span>
<span data-ttu-id="320bd-103">Crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="320bd-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="320bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="320bd-104">SYNTAX</span></span>

### <span data-ttu-id="320bd-105">Un blocco nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="320bd-105">A lock at the specified scope.</span></span> <span data-ttu-id="320bd-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="320bd-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320bd-107">Un blocco nell'ambito del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="320bd-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320bd-108">Un blocco nell'ambito delle risorse del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="320bd-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320bd-109">Un blocco nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="320bd-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320bd-110">Un blocco nell'ambito delle risorse dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="320bd-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320bd-111">Un blocco nell'ambito delle risorse del tenant.</span><span class="sxs-lookup"><span data-stu-id="320bd-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320bd-112">Un blocco, per ID.</span><span class="sxs-lookup"><span data-stu-id="320bd-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320bd-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="320bd-113">DESCRIPTION</span></span>
<span data-ttu-id="320bd-114">Il cmdlet **New-AzureRmResourceLock** crea un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="320bd-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="320bd-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="320bd-115">EXAMPLES</span></span>

### <span data-ttu-id="320bd-116">Esempio 1: creare un blocco delle risorse in un sito Web</span><span class="sxs-lookup"><span data-stu-id="320bd-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="320bd-117">Questo comando crea un blocco delle risorse in un sito Web.</span><span class="sxs-lookup"><span data-stu-id="320bd-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="320bd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="320bd-118">PARAMETERS</span></span>

### <span data-ttu-id="320bd-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="320bd-119">-ApiVersion</span></span>
<span data-ttu-id="320bd-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="320bd-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="320bd-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="320bd-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="320bd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="320bd-122">-Force</span></span>
<span data-ttu-id="320bd-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="320bd-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="320bd-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="320bd-124">-InformationAction</span></span>
<span data-ttu-id="320bd-125">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="320bd-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="320bd-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="320bd-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="320bd-127">Continuare</span><span class="sxs-lookup"><span data-stu-id="320bd-127">Continue</span></span>
- <span data-ttu-id="320bd-128">Ignora</span><span class="sxs-lookup"><span data-stu-id="320bd-128">Ignore</span></span>
- <span data-ttu-id="320bd-129">Informarsi</span><span class="sxs-lookup"><span data-stu-id="320bd-129">Inquire</span></span>
- <span data-ttu-id="320bd-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="320bd-130">SilentlyContinue</span></span>
- <span data-ttu-id="320bd-131">Stop</span><span class="sxs-lookup"><span data-stu-id="320bd-131">Stop</span></span>
- <span data-ttu-id="320bd-132">Sospensione</span><span class="sxs-lookup"><span data-stu-id="320bd-132">Suspend</span></span>

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

### <span data-ttu-id="320bd-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="320bd-133">-InformationVariable</span></span>
<span data-ttu-id="320bd-134">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="320bd-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="320bd-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="320bd-135">-LockId</span></span>
<span data-ttu-id="320bd-136">Specifica l'ID del blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="320bd-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="320bd-137">-LockLevel</span></span>
<span data-ttu-id="320bd-138">Specifica il livello per il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="320bd-139">Attualmente, l'unico valore valido è CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="320bd-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="320bd-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="320bd-140">-LockName</span></span>
<span data-ttu-id="320bd-141">Specifica il nome del blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="320bd-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="320bd-142">-LockNotes</span></span>
<span data-ttu-id="320bd-143">Specifica le note per il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="320bd-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="320bd-144">-Pre</span></span>
<span data-ttu-id="320bd-145">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="320bd-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="320bd-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320bd-146">-ResourceGroupName</span></span>
<span data-ttu-id="320bd-147">Specifica il nome di un gruppo di risorse per cui si applica il blocco o che contiene il gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="320bd-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="320bd-148">-ResourceName</span></span>
<span data-ttu-id="320bd-149">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="320bd-150">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="320bd-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="320bd-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="320bd-151">-ResourceType</span></span>
<span data-ttu-id="320bd-152">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="320bd-153">-Ambito</span><span class="sxs-lookup"><span data-stu-id="320bd-153">-Scope</span></span>
<span data-ttu-id="320bd-154">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="320bd-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="320bd-155">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="320bd-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="320bd-156">`/subscriptions/`nome del database del nome del gruppo di risorse ID abbonamento nome `/resourceGroups/` `/providers/Microsoft.Sql/servers/` server `/databases/`</span><span class="sxs-lookup"><span data-stu-id="320bd-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="320bd-157">Per specificare un gruppo di risorse, usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="320bd-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="320bd-158">`/subscriptions/`nome del `/resourceGroups/` gruppo di risorse ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="320bd-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="320bd-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="320bd-159">-TenantLevel</span></span>
<span data-ttu-id="320bd-160">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="320bd-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="320bd-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="320bd-161">-Confirm</span></span>
<span data-ttu-id="320bd-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320bd-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320bd-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320bd-163">-WhatIf</span></span>
<span data-ttu-id="320bd-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="320bd-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320bd-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="320bd-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320bd-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320bd-166">-DefaultProfile</span></span>
<span data-ttu-id="320bd-167">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="320bd-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="320bd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320bd-168">CommonParameters</span></span>
<span data-ttu-id="320bd-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320bd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320bd-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320bd-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320bd-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="320bd-171">INPUTS</span></span>

## <span data-ttu-id="320bd-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="320bd-172">OUTPUTS</span></span>

### <span data-ttu-id="320bd-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="320bd-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="320bd-174">Note</span><span class="sxs-lookup"><span data-stu-id="320bd-174">NOTES</span></span>

## <span data-ttu-id="320bd-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="320bd-175">RELATED LINKS</span></span>

[<span data-ttu-id="320bd-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="320bd-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="320bd-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="320bd-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="320bd-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="320bd-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


