---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: 4babe23fbddbc11838cad6307117884c3bb14ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990581"
---
# <span data-ttu-id="7169c-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="7169c-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="7169c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7169c-102">SYNOPSIS</span></span>
<span data-ttu-id="7169c-103">Elimina un archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7169c-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="7169c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7169c-104">SYNTAX</span></span>

### <span data-ttu-id="7169c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7169c-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7169c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7169c-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7169c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7169c-107">DESCRIPTION</span></span>
<span data-ttu-id="7169c-108">Elimina un archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7169c-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="7169c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7169c-109">EXAMPLES</span></span>

### <span data-ttu-id="7169c-110">Esempio 1: Rimuovere un archivio di configurazione delle app</span><span class="sxs-lookup"><span data-stu-id="7169c-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="7169c-111">Questo comando rimuove un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="7169c-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="7169c-112">Esempio 2: Rimuovere un archivio di configurazione delle app</span><span class="sxs-lookup"><span data-stu-id="7169c-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="7169c-113">Questo comando rimuove un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="7169c-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="7169c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7169c-114">PARAMETERS</span></span>

### <span data-ttu-id="7169c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7169c-115">-AsJob</span></span>
<span data-ttu-id="7169c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="7169c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7169c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7169c-117">-DefaultProfile</span></span>
<span data-ttu-id="7169c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7169c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7169c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7169c-119">-InputObject</span></span>
<span data-ttu-id="7169c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7169c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7169c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7169c-121">-Name</span></span>
<span data-ttu-id="7169c-122">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7169c-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7169c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7169c-123">-NoWait</span></span>
<span data-ttu-id="7169c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="7169c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7169c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7169c-125">-PassThru</span></span>
<span data-ttu-id="7169c-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="7169c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7169c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7169c-127">-ResourceGroupName</span></span>
<span data-ttu-id="7169c-128">Nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="7169c-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7169c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7169c-129">-SubscriptionId</span></span>
<span data-ttu-id="7169c-130">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7169c-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7169c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7169c-131">-Confirm</span></span>
<span data-ttu-id="7169c-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7169c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7169c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7169c-133">-WhatIf</span></span>
<span data-ttu-id="7169c-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7169c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7169c-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7169c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7169c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7169c-136">CommonParameters</span></span>
<span data-ttu-id="7169c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7169c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7169c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7169c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7169c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="7169c-139">INPUTS</span></span>

### <span data-ttu-id="7169c-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="7169c-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="7169c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7169c-141">OUTPUTS</span></span>

### <span data-ttu-id="7169c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7169c-142">System.Boolean</span></span>

## <span data-ttu-id="7169c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="7169c-143">NOTES</span></span>

<span data-ttu-id="7169c-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7169c-144">ALIASES</span></span>

<span data-ttu-id="7169c-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7169c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7169c-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7169c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7169c-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7169c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7169c-148">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7169c-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7169c-149">`[ConfigStoreName <String>]`: nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7169c-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="7169c-150">`[GroupName <String>]`: nome del gruppo di risorse collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7169c-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="7169c-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7169c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7169c-152">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="7169c-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="7169c-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="7169c-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="7169c-154">`[SubscriptionId <String>]`: ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7169c-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="7169c-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7169c-155">RELATED LINKS</span></span>

