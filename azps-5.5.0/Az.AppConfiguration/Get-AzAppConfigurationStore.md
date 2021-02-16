---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205587"
---
# <span data-ttu-id="64a10-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="64a10-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="64a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a10-102">SYNOPSIS</span></span>
<span data-ttu-id="64a10-103">Ottenere o elencare gli archivi di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="64a10-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="64a10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64a10-104">SYNTAX</span></span>

### <span data-ttu-id="64a10-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64a10-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64a10-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="64a10-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64a10-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64a10-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="64a10-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="64a10-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="64a10-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64a10-109">DESCRIPTION</span></span>
<span data-ttu-id="64a10-110">Ottenere o elencare gli archivi di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="64a10-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="64a10-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64a10-111">EXAMPLES</span></span>

### <span data-ttu-id="64a10-112">Esempio 1: Elencare tutti gli store di configurazione delle app in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="64a10-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="64a10-113">Questo comando elenca tutti gli store di configurazione delle app in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="64a10-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="64a10-114">Esempio 2: Elencare tutti gli archivi di configurazione delle app in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="64a10-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="64a10-115">Questo comando elenca tutti gli archivi di configurazione delle app in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64a10-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="64a10-116">Esempio 3: Ottenere un archivio di configurazione delle app in base al nome</span><span class="sxs-lookup"><span data-stu-id="64a10-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="64a10-117">Questo comando ottiene un archivio di configurazione delle app in base al nome.</span><span class="sxs-lookup"><span data-stu-id="64a10-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="64a10-118">Esempio 4: Ottenere un archivio di configurazione delle app tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="64a10-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="64a10-119">Questo comando ottiene un archivio di configurazione delle app tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="64a10-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="64a10-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a10-120">PARAMETERS</span></span>

### <span data-ttu-id="64a10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a10-121">-DefaultProfile</span></span>
<span data-ttu-id="64a10-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64a10-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a10-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a10-123">-InputObject</span></span>
<span data-ttu-id="64a10-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64a10-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a10-125">-Name</span><span class="sxs-lookup"><span data-stu-id="64a10-125">-Name</span></span>
<span data-ttu-id="64a10-126">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="64a10-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a10-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a10-127">-ResourceGroupName</span></span>
<span data-ttu-id="64a10-128">Nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="64a10-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a10-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64a10-129">-SubscriptionId</span></span>
<span data-ttu-id="64a10-130">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64a10-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a10-131">CommonParameters</span></span>
<span data-ttu-id="64a10-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a10-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64a10-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a10-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="64a10-134">INPUTS</span></span>

### <span data-ttu-id="64a10-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="64a10-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="64a10-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64a10-136">OUTPUTS</span></span>

### <span data-ttu-id="64a10-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="64a10-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="64a10-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="64a10-138">NOTES</span></span>

<span data-ttu-id="64a10-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="64a10-139">ALIASES</span></span>

<span data-ttu-id="64a10-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="64a10-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64a10-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="64a10-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64a10-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64a10-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64a10-143">INPUTOBJECT <IAppConfigurationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="64a10-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64a10-144">`[ConfigStoreName <String>]`: nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="64a10-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="64a10-145">`[GroupName <String>]`: nome del gruppo di risorse collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="64a10-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="64a10-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="64a10-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64a10-147">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="64a10-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="64a10-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="64a10-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="64a10-149">`[SubscriptionId <String>]`: ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64a10-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="64a10-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64a10-150">RELATED LINKS</span></span>

