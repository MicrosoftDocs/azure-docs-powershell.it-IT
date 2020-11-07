---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854778"
---
# <span data-ttu-id="532d9-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="532d9-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="532d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="532d9-102">SYNOPSIS</span></span>
<span data-ttu-id="532d9-103">Rimuove un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="532d9-103">Removes a resource lock.</span></span>

## <span data-ttu-id="532d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="532d9-104">SYNTAX</span></span>

### <span data-ttu-id="532d9-105">ByLockId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="532d9-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532d9-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="532d9-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532d9-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="532d9-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532d9-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="532d9-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532d9-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="532d9-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532d9-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="532d9-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="532d9-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="532d9-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="532d9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="532d9-112">DESCRIPTION</span></span>
<span data-ttu-id="532d9-113">Il cmdlet **Remove-AzResourceLock** rimuove un blocco di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="532d9-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="532d9-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="532d9-114">EXAMPLES</span></span>

### <span data-ttu-id="532d9-115">Esempio 1: rimuovere un blocco</span><span class="sxs-lookup"><span data-stu-id="532d9-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="532d9-116">Questo comando rimuove il blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="532d9-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="532d9-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="532d9-117">PARAMETERS</span></span>

### <span data-ttu-id="532d9-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="532d9-118">-ApiVersion</span></span>
<span data-ttu-id="532d9-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="532d9-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="532d9-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="532d9-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="532d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532d9-121">-DefaultProfile</span></span>
<span data-ttu-id="532d9-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="532d9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="532d9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="532d9-123">-Force</span></span>
<span data-ttu-id="532d9-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="532d9-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="532d9-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="532d9-125">-LockId</span></span>
<span data-ttu-id="532d9-126">Specifica l'ID del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="532d9-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="532d9-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="532d9-127">-LockName</span></span>
<span data-ttu-id="532d9-128">Specifica il nome del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="532d9-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="532d9-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="532d9-129">-Pre</span></span>
<span data-ttu-id="532d9-130">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="532d9-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="532d9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532d9-131">-ResourceGroupName</span></span>
<span data-ttu-id="532d9-132">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="532d9-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="532d9-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="532d9-133">-ResourceName</span></span>
<span data-ttu-id="532d9-134">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="532d9-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="532d9-135">Ad esempio, per specificare un database, usa il formato seguente: `/` database server</span><span class="sxs-lookup"><span data-stu-id="532d9-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="532d9-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="532d9-136">-ResourceType</span></span>
<span data-ttu-id="532d9-137">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="532d9-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="532d9-138">-Ambito</span><span class="sxs-lookup"><span data-stu-id="532d9-138">-Scope</span></span>
<span data-ttu-id="532d9-139">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="532d9-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="532d9-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="532d9-140">-TenantLevel</span></span>
<span data-ttu-id="532d9-141">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="532d9-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="532d9-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="532d9-142">-Confirm</span></span>
<span data-ttu-id="532d9-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="532d9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532d9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532d9-144">-WhatIf</span></span>
<span data-ttu-id="532d9-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="532d9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="532d9-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="532d9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532d9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532d9-147">CommonParameters</span></span>
<span data-ttu-id="532d9-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="532d9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532d9-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="532d9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532d9-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="532d9-150">INPUTS</span></span>

### <span data-ttu-id="532d9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="532d9-151">System.String</span></span>

## <span data-ttu-id="532d9-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="532d9-152">OUTPUTS</span></span>

### <span data-ttu-id="532d9-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="532d9-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="532d9-154">Note</span><span class="sxs-lookup"><span data-stu-id="532d9-154">NOTES</span></span>

## <span data-ttu-id="532d9-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="532d9-155">RELATED LINKS</span></span>

[<span data-ttu-id="532d9-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="532d9-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="532d9-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="532d9-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="532d9-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="532d9-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


