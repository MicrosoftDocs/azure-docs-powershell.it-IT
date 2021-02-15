---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182303"
---
# <span data-ttu-id="4c6c1-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4c6c1-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="4c6c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6c1-103">Crea un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4c6c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c6c1-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4c6c1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="4c6c1-106">Crea un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4c6c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c6c1-107">EXAMPLES</span></span>

### <span data-ttu-id="4c6c1-108">Esempio 1: Creare un archivio di configurazione delle app</span><span class="sxs-lookup"><span data-stu-id="4c6c1-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4c6c1-109">Questo comando crea un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="4c6c1-110">Esempio 2: Creare una configurazione dell'app con IdentityType impostato su "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="4c6c1-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4c6c1-111">Questo comando crea una configurazione dell'app e le assegna un'identità gestita assegnata all'utente.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="4c6c1-112">Vedere l'esempio `Update-AzAppConfigurationStore` di per la procedura seguente per abilitare CMK (chiave gestita cusomer).</span><span class="sxs-lookup"><span data-stu-id="4c6c1-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="4c6c1-113">Esempio 3: Creare una configurazione dell'app con IdentityType impostato su "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="4c6c1-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4c6c1-114">Questo comando crea una configurazione dell'app e abilita l'identità gestita assegnata al sistema associata alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="4c6c1-115">Vedere l'esempio `Update-AzAppConfigurationStore` di per la procedura seguente per abilitare CMK (chiave gestita cusomer).</span><span class="sxs-lookup"><span data-stu-id="4c6c1-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="4c6c1-116">Esempio 4: Creare una configurazione dell'app con IdentityType impostato su "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="4c6c1-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4c6c1-117">È possibile abilitare le identità gestite assegnate al sistema e allo stesso tempo assegnare le identità agli utenti.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="4c6c1-118">Vedere l'esempio `Update-AzAppConfigurationStore` di per la procedura seguente per abilitare CMK (chiave gestita cusomer).</span><span class="sxs-lookup"><span data-stu-id="4c6c1-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="4c6c1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c6c1-119">PARAMETERS</span></span>

### <span data-ttu-id="4c6c1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c6c1-120">-AsJob</span></span>
<span data-ttu-id="4c6c1-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4c6c1-121">Run the command as a job</span></span>

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

### <span data-ttu-id="4c6c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6c1-122">-DefaultProfile</span></span>
<span data-ttu-id="4c6c1-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4c6c1-124">-IdentityType</span></span>
<span data-ttu-id="4c6c1-125">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-125">The type of managed identity used.</span></span>
<span data-ttu-id="4c6c1-126">Il tipo 'SystemAssignedAndUserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="4c6c1-127">Il tipo "Nessuna" rimuove le identità.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-128">-Location</span><span class="sxs-lookup"><span data-stu-id="4c6c1-128">-Location</span></span>
<span data-ttu-id="4c6c1-129">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-129">The location of the resource.</span></span>
<span data-ttu-id="4c6c1-130">Non è possibile modificare questa impostazione dopo la creazione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4c6c1-131">-Name</span></span>
<span data-ttu-id="4c6c1-132">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4c6c1-133">-NoWait</span></span>
<span data-ttu-id="4c6c1-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4c6c1-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4c6c1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c6c1-135">-ResourceGroupName</span></span>
<span data-ttu-id="4c6c1-136">Nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="4c6c1-137">-Sku</span></span>
<span data-ttu-id="4c6c1-138">Nome SKU dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c6c1-139">-SubscriptionId</span></span>
<span data-ttu-id="4c6c1-140">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c6c1-141">-Tag</span></span>
<span data-ttu-id="4c6c1-142">Tag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-142">The tags of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4c6c1-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="4c6c1-144">Elenco delle identità assegnate dall'utente associate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="4c6c1-145">Le chiavi del dizionario di identità assegnate dall'utente saranno id di risorse nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'. ARM</span><span class="sxs-lookup"><span data-stu-id="4c6c1-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c6c1-146">-Confirm</span></span>
<span data-ttu-id="4c6c1-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6c1-148">-WhatIf</span></span>
<span data-ttu-id="4c6c1-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c6c1-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6c1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6c1-151">CommonParameters</span></span>
<span data-ttu-id="4c6c1-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6c1-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c6c1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6c1-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c6c1-154">INPUTS</span></span>

## <span data-ttu-id="4c6c1-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c6c1-155">OUTPUTS</span></span>

### <span data-ttu-id="4c6c1-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4c6c1-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="4c6c1-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c6c1-157">NOTES</span></span>

<span data-ttu-id="4c6c1-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4c6c1-158">ALIASES</span></span>

## <span data-ttu-id="4c6c1-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c6c1-159">RELATED LINKS</span></span>



[<span data-ttu-id="4c6c1-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4c6c1-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

