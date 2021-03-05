---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 38f9aef513e13b2676569d434977752f3d193062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985009"
---
# <span data-ttu-id="b4d35-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b4d35-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b4d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d35-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d35-103">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="b4d35-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="b4d35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4d35-104">SYNTAX</span></span>

### <span data-ttu-id="b4d35-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4d35-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4d35-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b4d35-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4d35-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d35-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d35-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="b4d35-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b4d35-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4d35-109">DESCRIPTION</span></span>
<span data-ttu-id="b4d35-110">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="b4d35-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="b4d35-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4d35-111">EXAMPLES</span></span>

### <span data-ttu-id="b4d35-112">Esempio 1: Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4d35-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b4d35-113">Ottenere tutti i digitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="b4d35-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="b4d35-114">Esempio 2: Ottenere</span><span class="sxs-lookup"><span data-stu-id="b4d35-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b4d35-115">Ottenere l'istanza specificata di AzDigitalTwinsInstance da ResourceName</span><span class="sxs-lookup"><span data-stu-id="b4d35-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="b4d35-116">Esempio 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d35-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b4d35-117">Ottenere l'istanza specificata di AzDigitalTwinsInstance per Object</span><span class="sxs-lookup"><span data-stu-id="b4d35-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="b4d35-118">Esempio 4: Elenco1</span><span class="sxs-lookup"><span data-stu-id="b4d35-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b4d35-119">Ottenere tutta DigitalTwinsInstance da ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d35-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="b4d35-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4d35-120">PARAMETERS</span></span>

### <span data-ttu-id="b4d35-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d35-121">-DefaultProfile</span></span>
<span data-ttu-id="b4d35-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d35-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d35-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d35-123">-InputObject</span></span>
<span data-ttu-id="b4d35-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b4d35-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4d35-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d35-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4d35-126">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b4d35-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b4d35-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b4d35-127">-ResourceName</span></span>
<span data-ttu-id="b4d35-128">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b4d35-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b4d35-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4d35-129">-SubscriptionId</span></span>
<span data-ttu-id="b4d35-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b4d35-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="b4d35-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d35-131">CommonParameters</span></span>
<span data-ttu-id="b4d35-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d35-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d35-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4d35-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d35-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4d35-134">INPUTS</span></span>

### <span data-ttu-id="b4d35-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d35-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b4d35-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4d35-136">OUTPUTS</span></span>

### <span data-ttu-id="b4d35-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b4d35-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b4d35-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4d35-138">NOTES</span></span>

<span data-ttu-id="b4d35-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b4d35-139">ALIASES</span></span>

<span data-ttu-id="b4d35-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b4d35-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4d35-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b4d35-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4d35-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4d35-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4d35-143">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b4d35-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4d35-144">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="b4d35-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b4d35-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b4d35-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4d35-146">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b4d35-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b4d35-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b4d35-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b4d35-148">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b4d35-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b4d35-149">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b4d35-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b4d35-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4d35-150">RELATED LINKS</span></span>

