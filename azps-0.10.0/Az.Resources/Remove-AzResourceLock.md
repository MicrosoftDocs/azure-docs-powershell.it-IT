---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862389"
---
# <span data-ttu-id="7f506-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f506-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="7f506-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f506-102">SYNOPSIS</span></span>
<span data-ttu-id="7f506-103">Rimuove un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f506-103">Removes a resource lock.</span></span>

## <span data-ttu-id="7f506-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f506-104">SYNTAX</span></span>

### <span data-ttu-id="7f506-105">ByLockId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f506-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f506-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f506-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f506-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="7f506-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f506-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="7f506-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f506-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="7f506-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f506-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7f506-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f506-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7f506-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f506-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f506-112">DESCRIPTION</span></span>
<span data-ttu-id="7f506-113">Il cmdlet **Remove-AzResourceLock** rimuove un blocco di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7f506-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="7f506-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f506-114">EXAMPLES</span></span>

### <span data-ttu-id="7f506-115">Esempio 1: rimuovere un blocco</span><span class="sxs-lookup"><span data-stu-id="7f506-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="7f506-116">Questo comando rimuove il blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="7f506-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="7f506-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f506-117">PARAMETERS</span></span>

### <span data-ttu-id="7f506-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f506-118">-ApiVersion</span></span>
<span data-ttu-id="7f506-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7f506-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7f506-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f506-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7f506-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f506-121">-DefaultProfile</span></span>
<span data-ttu-id="7f506-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f506-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f506-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7f506-123">-Force</span></span>
<span data-ttu-id="7f506-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7f506-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f506-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7f506-125">-InformationAction</span></span>
<span data-ttu-id="7f506-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7f506-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="7f506-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f506-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f506-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="7f506-128">Continue</span></span>
- <span data-ttu-id="7f506-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="7f506-129">Ignore</span></span>
- <span data-ttu-id="7f506-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7f506-130">Inquire</span></span>
- <span data-ttu-id="7f506-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f506-131">SilentlyContinue</span></span>
- <span data-ttu-id="7f506-132">Stop</span><span class="sxs-lookup"><span data-stu-id="7f506-132">Stop</span></span>
- <span data-ttu-id="7f506-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7f506-133">Suspend</span></span>

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

### <span data-ttu-id="7f506-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f506-134">-InformationVariable</span></span>
<span data-ttu-id="7f506-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f506-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f506-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="7f506-136">-LockId</span></span>
<span data-ttu-id="7f506-137">Specifica l'ID del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f506-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f506-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="7f506-138">-LockName</span></span>
<span data-ttu-id="7f506-139">Specifica il nome del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f506-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f506-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="7f506-140">-Pre</span></span>
<span data-ttu-id="7f506-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7f506-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7f506-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f506-142">-ResourceGroupName</span></span>
<span data-ttu-id="7f506-143">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f506-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="7f506-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7f506-144">-ResourceName</span></span>
<span data-ttu-id="7f506-145">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f506-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="7f506-146">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="7f506-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="7f506-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7f506-147">-ResourceType</span></span>
<span data-ttu-id="7f506-148">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f506-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="7f506-149">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7f506-149">-Scope</span></span>
<span data-ttu-id="7f506-150">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f506-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="7f506-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7f506-151">-TenantLevel</span></span>
<span data-ttu-id="7f506-152">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="7f506-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="7f506-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f506-153">-Confirm</span></span>
<span data-ttu-id="7f506-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f506-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f506-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f506-155">-WhatIf</span></span>
<span data-ttu-id="7f506-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f506-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f506-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f506-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f506-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f506-158">CommonParameters</span></span>
<span data-ttu-id="7f506-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f506-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f506-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f506-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f506-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f506-161">INPUTS</span></span>

## <span data-ttu-id="7f506-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f506-162">OUTPUTS</span></span>

## <span data-ttu-id="7f506-163">Note</span><span class="sxs-lookup"><span data-stu-id="7f506-163">NOTES</span></span>

## <span data-ttu-id="7f506-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f506-164">RELATED LINKS</span></span>

[<span data-ttu-id="7f506-165">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f506-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="7f506-166">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f506-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="7f506-167">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f506-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


