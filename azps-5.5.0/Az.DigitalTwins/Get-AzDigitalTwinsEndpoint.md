---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188511"
---
# <span data-ttu-id="45e37-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="45e37-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="45e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e37-102">SYNOPSIS</span></span>
<span data-ttu-id="45e37-103">Ottieni DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="45e37-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="45e37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45e37-104">SYNTAX</span></span>

### <span data-ttu-id="45e37-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45e37-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45e37-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="45e37-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45e37-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45e37-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="45e37-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45e37-108">DESCRIPTION</span></span>
<span data-ttu-id="45e37-109">Ottieni DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="45e37-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="45e37-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45e37-110">EXAMPLES</span></span>

### <span data-ttu-id="45e37-111">Esempio 1: Elenco AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45e37-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="45e37-112">Elencare tutti gli elementi AzDigitalTwinsEndpoints per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e37-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="45e37-113">Esempio 2: Ottenere AzDigitalTwinsEndpoint da EndpointName</span><span class="sxs-lookup"><span data-stu-id="45e37-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="45e37-114">Ottenere AzDigitalTwinsEndpoint da EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45e37-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="45e37-115">Esempio 3: Ottenere AzDigitalTwinsEndpoint per l'oggetto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="45e37-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="45e37-116">Ottenere AzDigitalTwinsEndpoint per oggetto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="45e37-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="45e37-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e37-117">PARAMETERS</span></span>

### <span data-ttu-id="45e37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e37-118">-DefaultProfile</span></span>
<span data-ttu-id="45e37-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45e37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45e37-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="45e37-120">-EndpointName</span></span>
<span data-ttu-id="45e37-121">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="45e37-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="45e37-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45e37-122">-InputObject</span></span>
<span data-ttu-id="45e37-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="45e37-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45e37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e37-124">-ResourceGroupName</span></span>
<span data-ttu-id="45e37-125">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="45e37-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="45e37-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="45e37-126">-ResourceName</span></span>
<span data-ttu-id="45e37-127">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="45e37-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="45e37-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45e37-128">-SubscriptionId</span></span>
<span data-ttu-id="45e37-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="45e37-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="45e37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e37-130">CommonParameters</span></span>
<span data-ttu-id="45e37-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e37-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45e37-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e37-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="45e37-133">INPUTS</span></span>

### <span data-ttu-id="45e37-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="45e37-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="45e37-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45e37-135">OUTPUTS</span></span>

### <span data-ttu-id="45e37-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="45e37-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="45e37-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="45e37-137">NOTES</span></span>

<span data-ttu-id="45e37-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45e37-138">ALIASES</span></span>

<span data-ttu-id="45e37-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="45e37-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45e37-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="45e37-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45e37-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45e37-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45e37-142">INPUTOBJECT <IDigitalTwinsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="45e37-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45e37-143">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="45e37-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="45e37-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="45e37-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45e37-145">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="45e37-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="45e37-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="45e37-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="45e37-147">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="45e37-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="45e37-148">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="45e37-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="45e37-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45e37-149">RELATED LINKS</span></span>

