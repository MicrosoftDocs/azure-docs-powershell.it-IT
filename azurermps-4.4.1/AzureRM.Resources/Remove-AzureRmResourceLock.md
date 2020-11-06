---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519517"
---
# <span data-ttu-id="d9ad4-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d9ad4-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="d9ad4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ad4-103">Rimuove un blocco di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9ad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9ad4-104">SYNTAX</span></span>

### <span data-ttu-id="d9ad4-105">Un blocco, per ID. (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9ad4-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-106">Un blocco nell'ambito del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-107">Un blocco nell'ambito delle risorse del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-108">Un blocco nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-109">Un blocco nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-110">Un blocco nell'ambito delle risorse dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9ad4-111">Un blocco nell'ambito delle risorse del tenant.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ad4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9ad4-112">DESCRIPTION</span></span>
<span data-ttu-id="d9ad4-113">Il cmdlet **Remove-AzureRmResourceLock** rimuove un blocco di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="d9ad4-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9ad4-114">EXAMPLES</span></span>

### <span data-ttu-id="d9ad4-115">Esempio 1: rimuovere un blocco</span><span class="sxs-lookup"><span data-stu-id="d9ad4-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="d9ad4-116">Questo comando rimuove il blocco denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="d9ad4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9ad4-117">PARAMETERS</span></span>

### <span data-ttu-id="d9ad4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9ad4-118">-ApiVersion</span></span>
<span data-ttu-id="d9ad4-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9ad4-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d9ad4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d9ad4-121">-Force</span></span>
<span data-ttu-id="d9ad4-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9ad4-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d9ad4-123">-InformationAction</span></span>
<span data-ttu-id="d9ad4-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d9ad4-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9ad4-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9ad4-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="d9ad4-126">Continue</span></span>
- <span data-ttu-id="d9ad4-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="d9ad4-127">Ignore</span></span>
- <span data-ttu-id="d9ad4-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d9ad4-128">Inquire</span></span>
- <span data-ttu-id="d9ad4-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d9ad4-129">SilentlyContinue</span></span>
- <span data-ttu-id="d9ad4-130">Stop</span><span class="sxs-lookup"><span data-stu-id="d9ad4-130">Stop</span></span>
- <span data-ttu-id="d9ad4-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d9ad4-131">Suspend</span></span>

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

### <span data-ttu-id="d9ad4-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d9ad4-132">-InformationVariable</span></span>
<span data-ttu-id="d9ad4-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d9ad4-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="d9ad4-134">-LockId</span></span>
<span data-ttu-id="d9ad4-135">Specifica l'ID del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9ad4-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="d9ad4-136">-LockName</span></span>
<span data-ttu-id="d9ad4-137">Specifica il nome del blocco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad4-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9ad4-138">-Pre</span></span>
<span data-ttu-id="d9ad4-139">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d9ad4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ad4-140">-ResourceGroupName</span></span>
<span data-ttu-id="d9ad4-141">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d9ad4-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d9ad4-142">-ResourceName</span></span>
<span data-ttu-id="d9ad4-143">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d9ad4-144">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="d9ad4-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="d9ad4-145">`/`Database server</span><span class="sxs-lookup"><span data-stu-id="d9ad4-145">Server`/`Database</span></span>

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

### <span data-ttu-id="d9ad4-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d9ad4-146">-ResourceType</span></span>
<span data-ttu-id="d9ad4-147">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="d9ad4-148">-Ambito</span><span class="sxs-lookup"><span data-stu-id="d9ad4-148">-Scope</span></span>
<span data-ttu-id="d9ad4-149">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="d9ad4-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d9ad4-150">-TenantLevel</span></span>
<span data-ttu-id="d9ad4-151">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="d9ad4-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9ad4-152">-Confirm</span></span>
<span data-ttu-id="d9ad4-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ad4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ad4-154">-WhatIf</span></span>
<span data-ttu-id="d9ad4-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ad4-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ad4-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ad4-157">-DefaultProfile</span></span>
<span data-ttu-id="d9ad4-158">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ad4-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ad4-159">CommonParameters</span></span>
<span data-ttu-id="d9ad4-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ad4-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ad4-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ad4-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ad4-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9ad4-162">INPUTS</span></span>

## <span data-ttu-id="d9ad4-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9ad4-163">OUTPUTS</span></span>

### <span data-ttu-id="d9ad4-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d9ad4-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d9ad4-165">Note</span><span class="sxs-lookup"><span data-stu-id="d9ad4-165">NOTES</span></span>

## <span data-ttu-id="d9ad4-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9ad4-166">RELATED LINKS</span></span>

[<span data-ttu-id="d9ad4-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d9ad4-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="d9ad4-168">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d9ad4-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="d9ad4-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d9ad4-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


