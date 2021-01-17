---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376876"
---
# <span data-ttu-id="20c34-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="20c34-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="20c34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20c34-102">SYNOPSIS</span></span>
<span data-ttu-id="20c34-103">Ottenere l'endpoint DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="20c34-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="20c34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20c34-104">SYNTAX</span></span>

### <span data-ttu-id="20c34-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20c34-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20c34-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="20c34-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20c34-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20c34-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="20c34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20c34-108">DESCRIPTION</span></span>
<span data-ttu-id="20c34-109">Ottenere l'endpoint DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="20c34-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="20c34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20c34-110">EXAMPLES</span></span>

### <span data-ttu-id="20c34-111">Esempio 1: elenco AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20c34-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="20c34-112">Elenca tutti i AzDigitalTwinsEndpoints di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c34-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="20c34-113">Esempio 2: ottenere AzDigitalTwinsEndpoint per EndpointName</span><span class="sxs-lookup"><span data-stu-id="20c34-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="20c34-114">Ottenere AzDigitalTwinsEndpoint da EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20c34-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="20c34-115">Esempio 3: ottenere AzDigitalTwinsEndpoint dall'oggetto ' AzDigitalTwinsEndpoint '</span><span class="sxs-lookup"><span data-stu-id="20c34-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="20c34-116">Ottenere AzDigitalTwinsEndpoint dall'oggetto ' AzDigitalTwinsEndpoint '</span><span class="sxs-lookup"><span data-stu-id="20c34-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="20c34-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20c34-117">PARAMETERS</span></span>

### <span data-ttu-id="20c34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c34-118">-DefaultProfile</span></span>
<span data-ttu-id="20c34-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20c34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c34-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="20c34-120">-EndpointName</span></span>
<span data-ttu-id="20c34-121">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="20c34-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="20c34-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20c34-122">-InputObject</span></span>
<span data-ttu-id="20c34-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="20c34-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c34-124">-ResourceGroupName</span></span>
<span data-ttu-id="20c34-125">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="20c34-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="20c34-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="20c34-126">-ResourceName</span></span>
<span data-ttu-id="20c34-127">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="20c34-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="20c34-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20c34-128">-SubscriptionId</span></span>
<span data-ttu-id="20c34-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="20c34-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c34-130">CommonParameters</span></span>
<span data-ttu-id="20c34-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c34-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c34-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20c34-133">INPUTS</span></span>

### <span data-ttu-id="20c34-134">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="20c34-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="20c34-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20c34-135">OUTPUTS</span></span>

### <span data-ttu-id="20c34-136">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="20c34-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="20c34-137">Note</span><span class="sxs-lookup"><span data-stu-id="20c34-137">NOTES</span></span>

<span data-ttu-id="20c34-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="20c34-138">ALIASES</span></span>

<span data-ttu-id="20c34-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20c34-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20c34-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="20c34-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20c34-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20c34-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20c34-142">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="20c34-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20c34-143">`[EndpointName <String>]`: Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="20c34-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="20c34-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="20c34-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20c34-145">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="20c34-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="20c34-146">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="20c34-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="20c34-147">`[ResourceName <String>]`: Nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="20c34-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="20c34-148">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="20c34-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="20c34-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20c34-149">RELATED LINKS</span></span>

