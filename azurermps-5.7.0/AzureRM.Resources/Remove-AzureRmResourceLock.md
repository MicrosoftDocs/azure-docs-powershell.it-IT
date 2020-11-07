---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686304"
---
# <span data-ttu-id="a5c83-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a5c83-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="a5c83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5c83-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c83-103">Rimuove un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5c83-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5c83-104">SYNTAX</span></span>

### <span data-ttu-id="a5c83-105">ByLockId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5c83-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c83-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5c83-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c83-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="a5c83-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c83-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="a5c83-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c83-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="a5c83-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c83-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a5c83-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c83-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a5c83-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5c83-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5c83-112">DESCRIPTION</span></span>
<span data-ttu-id="a5c83-113">Il cmdlet **Remove-AzureRmResourceLock** rimuove un blocco di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c83-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="a5c83-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5c83-114">EXAMPLES</span></span>

### <span data-ttu-id="a5c83-115">Esempio 1: rimuovere un blocco</span><span class="sxs-lookup"><span data-stu-id="a5c83-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="a5c83-116">Questo comando rimuove il blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="a5c83-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="a5c83-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5c83-117">PARAMETERS</span></span>

### <span data-ttu-id="a5c83-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a5c83-118">-ApiVersion</span></span>
<span data-ttu-id="a5c83-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a5c83-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a5c83-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="a5c83-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c83-121">-DefaultProfile</span></span>
<span data-ttu-id="a5c83-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a5c83-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c83-123">-Force</span></span>
<span data-ttu-id="a5c83-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a5c83-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a5c83-125">-InformationAction</span></span>
<span data-ttu-id="a5c83-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a5c83-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a5c83-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5c83-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5c83-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="a5c83-128">Continue</span></span>
- <span data-ttu-id="a5c83-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="a5c83-129">Ignore</span></span>
- <span data-ttu-id="a5c83-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a5c83-130">Inquire</span></span>
- <span data-ttu-id="a5c83-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a5c83-131">SilentlyContinue</span></span>
- <span data-ttu-id="a5c83-132">Stop</span><span class="sxs-lookup"><span data-stu-id="a5c83-132">Stop</span></span>
- <span data-ttu-id="a5c83-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a5c83-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a5c83-134">-InformationVariable</span></span>
<span data-ttu-id="a5c83-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a5c83-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="a5c83-136">-LockId</span></span>
<span data-ttu-id="a5c83-137">Specifica l'ID del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c83-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="a5c83-138">-LockName</span></span>
<span data-ttu-id="a5c83-139">Specifica il nome del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c83-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5c83-140">-Pre</span></span>
<span data-ttu-id="a5c83-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a5c83-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c83-142">-ResourceGroupName</span></span>
<span data-ttu-id="a5c83-143">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a5c83-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a5c83-144">-ResourceName</span></span>
<span data-ttu-id="a5c83-145">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a5c83-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a5c83-146">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a5c83-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a5c83-147">`/`Database server</span><span class="sxs-lookup"><span data-stu-id="a5c83-147">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a5c83-148">-ResourceType</span></span>
<span data-ttu-id="a5c83-149">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a5c83-149">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-150">-Ambito</span><span class="sxs-lookup"><span data-stu-id="a5c83-150">-Scope</span></span>
<span data-ttu-id="a5c83-151">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="a5c83-151">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a5c83-152">-TenantLevel</span></span>
<span data-ttu-id="a5c83-153">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="a5c83-153">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5c83-154">-Confirm</span></span>
<span data-ttu-id="a5c83-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c83-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c83-156">-WhatIf</span></span>
<span data-ttu-id="a5c83-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c83-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c83-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c83-158">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c83-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c83-159">CommonParameters</span></span>
<span data-ttu-id="a5c83-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c83-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c83-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c83-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c83-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5c83-162">INPUTS</span></span>

### <span data-ttu-id="a5c83-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5c83-163">None</span></span>
<span data-ttu-id="a5c83-164">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a5c83-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5c83-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5c83-165">OUTPUTS</span></span>

### <span data-ttu-id="a5c83-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a5c83-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a5c83-167">Note</span><span class="sxs-lookup"><span data-stu-id="a5c83-167">NOTES</span></span>

## <span data-ttu-id="a5c83-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5c83-168">RELATED LINKS</span></span>

[<span data-ttu-id="a5c83-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a5c83-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a5c83-170">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a5c83-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="a5c83-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a5c83-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


