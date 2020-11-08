---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191687"
---
# <span data-ttu-id="917a4-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="917a4-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="917a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="917a4-102">SYNOPSIS</span></span>
<span data-ttu-id="917a4-103">Elimina un archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="917a4-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="917a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="917a4-104">SYNTAX</span></span>

### <span data-ttu-id="917a4-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="917a4-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="917a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="917a4-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="917a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="917a4-107">DESCRIPTION</span></span>
<span data-ttu-id="917a4-108">Elimina un archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="917a4-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="917a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="917a4-109">EXAMPLES</span></span>

### <span data-ttu-id="917a4-110">Esempio 1: rimuovere un archivio di configurazione dell'app</span><span class="sxs-lookup"><span data-stu-id="917a4-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="917a4-111">Questo comando rimuove un archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="917a4-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="917a4-112">Esempio 2: rimuovere un archivio di configurazione dell'app</span><span class="sxs-lookup"><span data-stu-id="917a4-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="917a4-113">Questo comando rimuove un archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="917a4-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="917a4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="917a4-114">PARAMETERS</span></span>

### <span data-ttu-id="917a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="917a4-115">-AsJob</span></span>
<span data-ttu-id="917a4-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="917a4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="917a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917a4-117">-DefaultProfile</span></span>
<span data-ttu-id="917a4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="917a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="917a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="917a4-119">-InputObject</span></span>
<span data-ttu-id="917a4-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="917a4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="917a4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="917a4-121">-Name</span></span>
<span data-ttu-id="917a4-122">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="917a4-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="917a4-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="917a4-123">-NoWait</span></span>
<span data-ttu-id="917a4-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="917a4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="917a4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="917a4-125">-PassThru</span></span>
<span data-ttu-id="917a4-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="917a4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="917a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="917a4-128">Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="917a4-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="917a4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="917a4-129">-SubscriptionId</span></span>
<span data-ttu-id="917a4-130">ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="917a4-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="917a4-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="917a4-131">-Confirm</span></span>
<span data-ttu-id="917a4-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="917a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917a4-133">-WhatIf</span></span>
<span data-ttu-id="917a4-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="917a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="917a4-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="917a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917a4-136">CommonParameters</span></span>
<span data-ttu-id="917a4-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917a4-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="917a4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917a4-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="917a4-139">INPUTS</span></span>

### <span data-ttu-id="917a4-140">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="917a4-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="917a4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="917a4-141">OUTPUTS</span></span>

### <span data-ttu-id="917a4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="917a4-142">System.Boolean</span></span>

## <span data-ttu-id="917a4-143">Note</span><span class="sxs-lookup"><span data-stu-id="917a4-143">NOTES</span></span>

<span data-ttu-id="917a4-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="917a4-144">ALIASES</span></span>

<span data-ttu-id="917a4-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="917a4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="917a4-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="917a4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="917a4-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="917a4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="917a4-148">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="917a4-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="917a4-149">`[ConfigStoreName <String>]`: Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="917a4-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="917a4-150">`[GroupName <String>]`: Nome del gruppo di risorse private link.</span><span class="sxs-lookup"><span data-stu-id="917a4-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="917a4-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="917a4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="917a4-152">`[PrivateEndpointConnectionName <String>]`: Nome connessione endpoint privato</span><span class="sxs-lookup"><span data-stu-id="917a4-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="917a4-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="917a4-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="917a4-154">`[SubscriptionId <String>]`: ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="917a4-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="917a4-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="917a4-155">RELATED LINKS</span></span>

