---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: fdf60c029f260d30aae8983165cbfb4d20203824
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866426"
---
# <span data-ttu-id="faa3f-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="faa3f-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="faa3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faa3f-102">SYNOPSIS</span></span>
<span data-ttu-id="faa3f-103">Rimuove un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="faa3f-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faa3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faa3f-104">SYNTAX</span></span>

### <span data-ttu-id="faa3f-105">ByLockId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="faa3f-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa3f-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="faa3f-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa3f-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="faa3f-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faa3f-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="faa3f-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa3f-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="faa3f-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa3f-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="faa3f-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faa3f-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="faa3f-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faa3f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faa3f-112">DESCRIPTION</span></span>
<span data-ttu-id="faa3f-113">Il cmdlet **Remove-AzureRmResourceLock** rimuove un blocco di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="faa3f-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="faa3f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faa3f-114">EXAMPLES</span></span>

### <span data-ttu-id="faa3f-115">Esempio 1: rimuovere un blocco</span><span class="sxs-lookup"><span data-stu-id="faa3f-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="faa3f-116">Questo comando rimuove il blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="faa3f-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="faa3f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faa3f-117">PARAMETERS</span></span>

### <span data-ttu-id="faa3f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="faa3f-118">-ApiVersion</span></span>
<span data-ttu-id="faa3f-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="faa3f-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="faa3f-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="faa3f-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="faa3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa3f-121">-DefaultProfile</span></span>
<span data-ttu-id="faa3f-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="faa3f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="faa3f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="faa3f-123">-Force</span></span>
<span data-ttu-id="faa3f-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="faa3f-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="faa3f-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="faa3f-125">-InformationAction</span></span>
<span data-ttu-id="faa3f-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="faa3f-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="faa3f-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="faa3f-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="faa3f-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="faa3f-128">Continue</span></span>
- <span data-ttu-id="faa3f-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="faa3f-129">Ignore</span></span>
- <span data-ttu-id="faa3f-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="faa3f-130">Inquire</span></span>
- <span data-ttu-id="faa3f-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="faa3f-131">SilentlyContinue</span></span>
- <span data-ttu-id="faa3f-132">Stop</span><span class="sxs-lookup"><span data-stu-id="faa3f-132">Stop</span></span>
- <span data-ttu-id="faa3f-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="faa3f-133">Suspend</span></span>

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

### <span data-ttu-id="faa3f-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="faa3f-134">-InformationVariable</span></span>
<span data-ttu-id="faa3f-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="faa3f-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="faa3f-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="faa3f-136">-LockId</span></span>
<span data-ttu-id="faa3f-137">Specifica l'ID del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa3f-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="faa3f-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="faa3f-138">-LockName</span></span>
<span data-ttu-id="faa3f-139">Specifica il nome del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa3f-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa3f-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="faa3f-140">-Pre</span></span>
<span data-ttu-id="faa3f-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="faa3f-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="faa3f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa3f-142">-ResourceGroupName</span></span>
<span data-ttu-id="faa3f-143">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="faa3f-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="faa3f-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="faa3f-144">-ResourceName</span></span>
<span data-ttu-id="faa3f-145">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="faa3f-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="faa3f-146">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="faa3f-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="faa3f-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="faa3f-147">-ResourceType</span></span>
<span data-ttu-id="faa3f-148">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="faa3f-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="faa3f-149">-Ambito</span><span class="sxs-lookup"><span data-stu-id="faa3f-149">-Scope</span></span>
<span data-ttu-id="faa3f-150">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="faa3f-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="faa3f-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="faa3f-151">-TenantLevel</span></span>
<span data-ttu-id="faa3f-152">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="faa3f-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="faa3f-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="faa3f-153">-Confirm</span></span>
<span data-ttu-id="faa3f-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa3f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa3f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa3f-155">-WhatIf</span></span>
<span data-ttu-id="faa3f-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa3f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa3f-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa3f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa3f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa3f-158">CommonParameters</span></span>
<span data-ttu-id="faa3f-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa3f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa3f-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa3f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa3f-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faa3f-161">INPUTS</span></span>

## <span data-ttu-id="faa3f-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faa3f-162">OUTPUTS</span></span>

## <span data-ttu-id="faa3f-163">Note</span><span class="sxs-lookup"><span data-stu-id="faa3f-163">NOTES</span></span>

## <span data-ttu-id="faa3f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faa3f-164">RELATED LINKS</span></span>

[<span data-ttu-id="faa3f-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="faa3f-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="faa3f-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="faa3f-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="faa3f-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="faa3f-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


