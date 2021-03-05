---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 35ba036e38b54a335cbdcdd923008a5a4ce055fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985023"
---
# <span data-ttu-id="4f69f-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f69f-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="4f69f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f69f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f69f-103">Ottieni DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="4f69f-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="4f69f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f69f-104">SYNTAX</span></span>

### <span data-ttu-id="4f69f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f69f-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4f69f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4f69f-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4f69f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f69f-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f69f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f69f-108">DESCRIPTION</span></span>
<span data-ttu-id="4f69f-109">Ottieni DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="4f69f-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="4f69f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f69f-110">EXAMPLES</span></span>

### <span data-ttu-id="4f69f-111">Esempio 1: Elenco AzDigitalTwinsEndpoint in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f69f-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="4f69f-112">Elencare tutti i valori AzDigitalTwinsEndpoints per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f69f-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="4f69f-113">Esempio 2: Ottenere AzDigitalTwinsEndpoint da EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f69f-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="4f69f-114">Ottenere AzDigitalTwinsEndpoint da EndpointName in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f69f-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="4f69f-115">Esempio 3: Ottenere AzDigitalTwinsEndpoint per l'oggetto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="4f69f-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="4f69f-116">Ottenere AzDigitalTwinsEndpoint per oggetto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="4f69f-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="4f69f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f69f-117">PARAMETERS</span></span>

### <span data-ttu-id="4f69f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f69f-118">-DefaultProfile</span></span>
<span data-ttu-id="4f69f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f69f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f69f-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f69f-120">-EndpointName</span></span>
<span data-ttu-id="4f69f-121">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="4f69f-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="4f69f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f69f-122">-InputObject</span></span>
<span data-ttu-id="4f69f-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4f69f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f69f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f69f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f69f-125">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4f69f-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4f69f-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4f69f-126">-ResourceName</span></span>
<span data-ttu-id="4f69f-127">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4f69f-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4f69f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f69f-128">-SubscriptionId</span></span>
<span data-ttu-id="4f69f-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f69f-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="4f69f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f69f-130">CommonParameters</span></span>
<span data-ttu-id="4f69f-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f69f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f69f-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f69f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f69f-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f69f-133">INPUTS</span></span>

### <span data-ttu-id="4f69f-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4f69f-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4f69f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f69f-135">OUTPUTS</span></span>

### <span data-ttu-id="4f69f-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="4f69f-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="4f69f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f69f-137">NOTES</span></span>

<span data-ttu-id="4f69f-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4f69f-138">ALIASES</span></span>

<span data-ttu-id="4f69f-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4f69f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f69f-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4f69f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f69f-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f69f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f69f-142">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4f69f-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f69f-143">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="4f69f-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4f69f-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4f69f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f69f-145">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4f69f-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f69f-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4f69f-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f69f-147">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4f69f-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f69f-148">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f69f-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4f69f-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f69f-149">RELATED LINKS</span></span>

