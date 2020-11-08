---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192516"
---
# <span data-ttu-id="72d85-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="72d85-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="72d85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72d85-102">SYNOPSIS</span></span>
<span data-ttu-id="72d85-103">Ottiene l'HSM dedicato di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="72d85-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="72d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72d85-104">SYNTAX</span></span>

### <span data-ttu-id="72d85-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72d85-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="72d85-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="72d85-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72d85-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72d85-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72d85-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="72d85-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72d85-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72d85-109">DESCRIPTION</span></span>
<span data-ttu-id="72d85-110">Ottiene l'HSM dedicato di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="72d85-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="72d85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72d85-111">EXAMPLES</span></span>

### <span data-ttu-id="72d85-112">Esempio 1: ottenere tutti i HSM dedicati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="72d85-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="72d85-113">Questo comando ottiene tutti i HSM dedicati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="72d85-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="72d85-114">Esempio 2: ottenere tutti i HSM dedicati in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72d85-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="72d85-115">Questo comando ottiene tutti i HSM dedicati in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72d85-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="72d85-116">Esempio 3: ottenere un HSM dedicato per nome</span><span class="sxs-lookup"><span data-stu-id="72d85-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="72d85-117">Questo comando ottiene un HSM dedicato per nome.</span><span class="sxs-lookup"><span data-stu-id="72d85-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="72d85-118">Esempio 4: ottenere un HSM dedicato per oggetto</span><span class="sxs-lookup"><span data-stu-id="72d85-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="72d85-119">Questo comando ottiene un HSM dedicato per oggetto.</span><span class="sxs-lookup"><span data-stu-id="72d85-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="72d85-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72d85-120">PARAMETERS</span></span>

### <span data-ttu-id="72d85-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d85-121">-DefaultProfile</span></span>
<span data-ttu-id="72d85-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72d85-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d85-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72d85-123">-InputObject</span></span>
<span data-ttu-id="72d85-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="72d85-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72d85-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="72d85-125">-Name</span></span>
<span data-ttu-id="72d85-126">Nome dell'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="72d85-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="72d85-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d85-127">-ResourceGroupName</span></span>
<span data-ttu-id="72d85-128">Il nome del gruppo di risorse a cui appartiene l'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="72d85-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="72d85-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72d85-129">-SubscriptionId</span></span>
<span data-ttu-id="72d85-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="72d85-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="72d85-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="72d85-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="72d85-132">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="72d85-132">-Top</span></span>
<span data-ttu-id="72d85-133">Numero massimo di risultati da restituire.</span><span class="sxs-lookup"><span data-stu-id="72d85-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="72d85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d85-134">CommonParameters</span></span>
<span data-ttu-id="72d85-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d85-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72d85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d85-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72d85-137">INPUTS</span></span>

### <span data-ttu-id="72d85-138">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="72d85-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="72d85-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72d85-139">OUTPUTS</span></span>

### <span data-ttu-id="72d85-140">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="72d85-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="72d85-141">Note</span><span class="sxs-lookup"><span data-stu-id="72d85-141">NOTES</span></span>

<span data-ttu-id="72d85-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72d85-142">ALIASES</span></span>

<span data-ttu-id="72d85-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72d85-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72d85-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="72d85-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72d85-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72d85-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72d85-146">INPUTOBJECT <IDedicatedHsmIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="72d85-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72d85-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="72d85-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72d85-148">`[Name <String>]`: Nome dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="72d85-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="72d85-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="72d85-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="72d85-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="72d85-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="72d85-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="72d85-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="72d85-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72d85-152">RELATED LINKS</span></span>

