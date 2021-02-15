---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204163"
---
# <span data-ttu-id="5e468-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5e468-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5e468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e468-102">SYNOPSIS</span></span>
<span data-ttu-id="5e468-103">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="5e468-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="5e468-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e468-104">SYNTAX</span></span>

### <span data-ttu-id="5e468-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e468-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e468-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5e468-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e468-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e468-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e468-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="5e468-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5e468-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e468-109">DESCRIPTION</span></span>
<span data-ttu-id="5e468-110">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="5e468-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="5e468-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e468-111">EXAMPLES</span></span>

### <span data-ttu-id="5e468-112">Esempio 1: Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e468-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5e468-113">Ottenere tutti i digitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="5e468-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="5e468-114">Esempio 2: Ottenere</span><span class="sxs-lookup"><span data-stu-id="5e468-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5e468-115">Ottenere l'istanza specificata di AzDigitalTwinsInstance da ResourceName</span><span class="sxs-lookup"><span data-stu-id="5e468-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="5e468-116">Esempio 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e468-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5e468-117">Ottenere l'istanza specificata di AzDigitalTwinsInstance in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="5e468-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="5e468-118">Esempio 4: Elenco1</span><span class="sxs-lookup"><span data-stu-id="5e468-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5e468-119">Ottenere tutta DigitalTwinsInstance da ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e468-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="5e468-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e468-120">PARAMETERS</span></span>

### <span data-ttu-id="5e468-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e468-121">-DefaultProfile</span></span>
<span data-ttu-id="5e468-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e468-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e468-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e468-123">-InputObject</span></span>
<span data-ttu-id="5e468-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5e468-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e468-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e468-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e468-126">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5e468-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5e468-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5e468-127">-ResourceName</span></span>
<span data-ttu-id="5e468-128">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5e468-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5e468-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e468-129">-SubscriptionId</span></span>
<span data-ttu-id="5e468-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5e468-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="5e468-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e468-131">CommonParameters</span></span>
<span data-ttu-id="5e468-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e468-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e468-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e468-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e468-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e468-134">INPUTS</span></span>

### <span data-ttu-id="5e468-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="5e468-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="5e468-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e468-136">OUTPUTS</span></span>

### <span data-ttu-id="5e468-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5e468-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5e468-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e468-138">NOTES</span></span>

<span data-ttu-id="5e468-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e468-139">ALIASES</span></span>

<span data-ttu-id="5e468-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="5e468-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e468-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5e468-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e468-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e468-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e468-143">INPUTOBJECT <IDigitalTwinsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="5e468-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e468-144">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="5e468-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="5e468-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="5e468-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e468-146">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5e468-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e468-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5e468-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e468-148">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5e468-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5e468-149">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5e468-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="5e468-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e468-150">RELATED LINKS</span></span>

