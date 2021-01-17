---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381499"
---
# <span data-ttu-id="c9f74-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="c9f74-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="c9f74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9f74-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f74-103">Ottenere o elencare gli archivi di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="c9f74-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="c9f74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9f74-104">SYNTAX</span></span>

### <span data-ttu-id="c9f74-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9f74-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9f74-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c9f74-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9f74-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9f74-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9f74-108">List1</span><span class="sxs-lookup"><span data-stu-id="c9f74-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9f74-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9f74-109">DESCRIPTION</span></span>
<span data-ttu-id="c9f74-110">Ottenere o elencare gli archivi di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="c9f74-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="c9f74-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9f74-111">EXAMPLES</span></span>

### <span data-ttu-id="c9f74-112">Esempio 1: elenca tutti gli archivi di configurazione dell'app in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="c9f74-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="c9f74-113">Questo comando elenca tutti gli archivi di configurazione delle app in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c9f74-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="c9f74-114">Esempio 2: elenca tutti gli archivi di configurazione delle app in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c9f74-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="c9f74-115">Questo comando elenca tutti gli archivi di configurazione delle app in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9f74-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="c9f74-116">Esempio 3: ottenere un archivio di configurazione dell'app in base al nome</span><span class="sxs-lookup"><span data-stu-id="c9f74-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="c9f74-117">Questo comando ottiene un archivio di configurazione dell'app in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c9f74-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="c9f74-118">Esempio 4: ottenere un archivio di configurazione dell'app in base alla pipeline</span><span class="sxs-lookup"><span data-stu-id="c9f74-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="c9f74-119">Questo comando ottiene un archivio di configurazione dell'app in base alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9f74-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="c9f74-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9f74-120">PARAMETERS</span></span>

### <span data-ttu-id="c9f74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f74-121">-DefaultProfile</span></span>
<span data-ttu-id="c9f74-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f74-123">-InputObject</span></span>
<span data-ttu-id="c9f74-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c9f74-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9f74-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9f74-125">-Name</span></span>
<span data-ttu-id="c9f74-126">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c9f74-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="c9f74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f74-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9f74-128">Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c9f74-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="c9f74-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9f74-129">-SubscriptionId</span></span>
<span data-ttu-id="c9f74-130">ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f74-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="c9f74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f74-131">CommonParameters</span></span>
<span data-ttu-id="c9f74-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f74-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9f74-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f74-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9f74-134">INPUTS</span></span>

### <span data-ttu-id="c9f74-135">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="c9f74-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="c9f74-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9f74-136">OUTPUTS</span></span>

### <span data-ttu-id="c9f74-137">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="c9f74-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="c9f74-138">Note</span><span class="sxs-lookup"><span data-stu-id="c9f74-138">NOTES</span></span>

<span data-ttu-id="c9f74-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c9f74-139">ALIASES</span></span>

<span data-ttu-id="c9f74-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9f74-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9f74-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c9f74-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9f74-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9f74-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9f74-143">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c9f74-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9f74-144">`[ConfigStoreName <String>]`: Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c9f74-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="c9f74-145">`[GroupName <String>]`: Nome del gruppo di risorse private link.</span><span class="sxs-lookup"><span data-stu-id="c9f74-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="c9f74-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c9f74-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9f74-147">`[PrivateEndpointConnectionName <String>]`: Nome connessione endpoint privato</span><span class="sxs-lookup"><span data-stu-id="c9f74-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="c9f74-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c9f74-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="c9f74-149">`[SubscriptionId <String>]`: ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f74-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="c9f74-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9f74-150">RELATED LINKS</span></span>

