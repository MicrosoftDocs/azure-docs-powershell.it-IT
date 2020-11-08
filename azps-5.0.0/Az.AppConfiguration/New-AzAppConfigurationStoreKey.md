---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199910"
---
# <span data-ttu-id="e73be-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="e73be-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="e73be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e73be-102">SYNOPSIS</span></span>
<span data-ttu-id="e73be-103">Rigenera un tasto di scelta per l'archivio di configurazione specificato.</span><span class="sxs-lookup"><span data-stu-id="e73be-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="e73be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e73be-104">SYNTAX</span></span>

### <span data-ttu-id="e73be-105">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e73be-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e73be-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e73be-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e73be-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73be-107">DESCRIPTION</span></span>
<span data-ttu-id="e73be-108">Rigenera un tasto di scelta per l'archivio di configurazione specificato.</span><span class="sxs-lookup"><span data-stu-id="e73be-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="e73be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e73be-109">EXAMPLES</span></span>

### <span data-ttu-id="e73be-110">Esempio 1: chiave di rigenerazione di un archivio di configurazione dell'app</span><span class="sxs-lookup"><span data-stu-id="e73be-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="e73be-111">Questo comando rigenera la chiave di un archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="e73be-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="e73be-112">Esempio 2: rigenerare la chiave di un archivio di configurazione dell'app per oggetto</span><span class="sxs-lookup"><span data-stu-id="e73be-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="e73be-113">Questo comando rigenera la chiave di un archivio di configurazione dell'app per oggetto.</span><span class="sxs-lookup"><span data-stu-id="e73be-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="e73be-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e73be-114">PARAMETERS</span></span>

### <span data-ttu-id="e73be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73be-115">-DefaultProfile</span></span>
<span data-ttu-id="e73be-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e73be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e73be-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e73be-117">-Id</span></span>
<span data-ttu-id="e73be-118">ID della chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="e73be-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="e73be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e73be-119">-InputObject</span></span>
<span data-ttu-id="e73be-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e73be-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e73be-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e73be-121">-Name</span></span>
<span data-ttu-id="e73be-122">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e73be-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73be-123">-ResourceGroupName</span></span>
<span data-ttu-id="e73be-124">Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e73be-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73be-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e73be-125">-SubscriptionId</span></span>
<span data-ttu-id="e73be-126">ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e73be-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73be-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e73be-127">-Confirm</span></span>
<span data-ttu-id="e73be-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e73be-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e73be-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73be-129">-WhatIf</span></span>
<span data-ttu-id="e73be-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e73be-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73be-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e73be-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e73be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73be-132">CommonParameters</span></span>
<span data-ttu-id="e73be-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73be-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e73be-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73be-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e73be-135">INPUTS</span></span>

### <span data-ttu-id="e73be-136">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="e73be-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="e73be-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e73be-137">OUTPUTS</span></span>

### <span data-ttu-id="e73be-138">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="e73be-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="e73be-139">Note</span><span class="sxs-lookup"><span data-stu-id="e73be-139">NOTES</span></span>

<span data-ttu-id="e73be-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e73be-140">ALIASES</span></span>

<span data-ttu-id="e73be-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e73be-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e73be-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e73be-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e73be-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e73be-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e73be-144">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e73be-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e73be-145">`[ConfigStoreName <String>]`: Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e73be-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="e73be-146">`[GroupName <String>]`: Nome del gruppo di risorse private link.</span><span class="sxs-lookup"><span data-stu-id="e73be-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="e73be-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e73be-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e73be-148">`[PrivateEndpointConnectionName <String>]`: Nome connessione endpoint privato</span><span class="sxs-lookup"><span data-stu-id="e73be-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="e73be-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e73be-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="e73be-150">`[SubscriptionId <String>]`: ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e73be-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="e73be-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e73be-151">RELATED LINKS</span></span>
