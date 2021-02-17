---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198030"
---
# <span data-ttu-id="e946b-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e946b-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="e946b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e946b-102">SYNOPSIS</span></span>
<span data-ttu-id="e946b-103">Ottiene l'HSM dedicato di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e946b-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="e946b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e946b-104">SYNTAX</span></span>

### <span data-ttu-id="e946b-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e946b-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e946b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e946b-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e946b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e946b-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e946b-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="e946b-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e946b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e946b-109">DESCRIPTION</span></span>
<span data-ttu-id="e946b-110">Ottiene l'HSM dedicato di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e946b-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="e946b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e946b-111">EXAMPLES</span></span>

### <span data-ttu-id="e946b-112">Esempio 1: Ottieni tutto il servizio HSM dedicato in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="e946b-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e946b-113">Questo comando recupera tutti gli elementi Dedicated HSM in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="e946b-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="e946b-114">Esempio 2: Ottieni tutto il servizio HSM dedicato in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e946b-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e946b-115">Questo comando recupera tutte le risorse Dedicated HSM in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e946b-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="e946b-116">Esempio 3: Ottenere un HSM dedicato in base al nome</span><span class="sxs-lookup"><span data-stu-id="e946b-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e946b-117">Questo comando ottiene un servizio HSM dedicato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e946b-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="e946b-118">Esempio 4: Ottenere un HSM dedicato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="e946b-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e946b-119">Questo comando ottiene un HSM dedicato in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e946b-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="e946b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e946b-120">PARAMETERS</span></span>

### <span data-ttu-id="e946b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e946b-121">-DefaultProfile</span></span>
<span data-ttu-id="e946b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e946b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e946b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e946b-123">-InputObject</span></span>
<span data-ttu-id="e946b-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e946b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e946b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e946b-125">-Name</span></span>
<span data-ttu-id="e946b-126">Il nome del servizio HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="e946b-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="e946b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e946b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e946b-128">Nome del gruppo di risorse a cui appartiene l'hsm dedicato.</span><span class="sxs-lookup"><span data-stu-id="e946b-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e946b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e946b-129">-SubscriptionId</span></span>
<span data-ttu-id="e946b-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e946b-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e946b-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e946b-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e946b-132">-In alto</span><span class="sxs-lookup"><span data-stu-id="e946b-132">-Top</span></span>
<span data-ttu-id="e946b-133">Numero massimo di risultati da restituire.</span><span class="sxs-lookup"><span data-stu-id="e946b-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e946b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e946b-134">CommonParameters</span></span>
<span data-ttu-id="e946b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e946b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e946b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e946b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e946b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e946b-137">INPUTS</span></span>

### <span data-ttu-id="e946b-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="e946b-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="e946b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e946b-139">OUTPUTS</span></span>

### <span data-ttu-id="e946b-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e946b-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="e946b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e946b-141">NOTES</span></span>

<span data-ttu-id="e946b-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e946b-142">ALIASES</span></span>

<span data-ttu-id="e946b-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e946b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e946b-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e946b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e946b-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e946b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e946b-146">INPUTOBJECT <IDedicatedHsmIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e946b-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e946b-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e946b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e946b-148">`[Name <String>]`: nome dell'Hsm dedicato</span><span class="sxs-lookup"><span data-stu-id="e946b-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="e946b-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e946b-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="e946b-150">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e946b-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e946b-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e946b-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e946b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e946b-152">RELATED LINKS</span></span>

