---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347020"
---
# <span data-ttu-id="f28b5-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="f28b5-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="f28b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f28b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f28b5-103">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="f28b5-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="f28b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f28b5-104">SYNTAX</span></span>

### <span data-ttu-id="f28b5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f28b5-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f28b5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f28b5-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f28b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f28b5-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f28b5-108">List1</span><span class="sxs-lookup"><span data-stu-id="f28b5-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f28b5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f28b5-109">DESCRIPTION</span></span>
<span data-ttu-id="f28b5-110">Ottenere la risorsa DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="f28b5-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="f28b5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f28b5-111">EXAMPLES</span></span>

### <span data-ttu-id="f28b5-112">Esempio 1: elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f28b5-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="f28b5-113">Ottenere tutte le DigitalTwinsInstance per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f28b5-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="f28b5-114">Esempio 2: ottenere</span><span class="sxs-lookup"><span data-stu-id="f28b5-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="f28b5-115">Ottieni il AzDigitalTwinsInstance specificato da resourceName</span><span class="sxs-lookup"><span data-stu-id="f28b5-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="f28b5-116">Esempio 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f28b5-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="f28b5-117">Ottenere l'oggetto AzDigitalTwinsInstance specificato per Object</span><span class="sxs-lookup"><span data-stu-id="f28b5-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="f28b5-118">Esempio 4: List1</span><span class="sxs-lookup"><span data-stu-id="f28b5-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="f28b5-119">Ottenere tutte le DigitalTwinsInstance da ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28b5-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="f28b5-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f28b5-120">PARAMETERS</span></span>

### <span data-ttu-id="f28b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28b5-121">-DefaultProfile</span></span>
<span data-ttu-id="f28b5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f28b5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28b5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f28b5-123">-InputObject</span></span>
<span data-ttu-id="f28b5-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f28b5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f28b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="f28b5-126">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f28b5-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f28b5-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f28b5-127">-ResourceName</span></span>
<span data-ttu-id="f28b5-128">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f28b5-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f28b5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f28b5-129">-SubscriptionId</span></span>
<span data-ttu-id="f28b5-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f28b5-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="f28b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28b5-131">CommonParameters</span></span>
<span data-ttu-id="f28b5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28b5-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f28b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28b5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f28b5-134">INPUTS</span></span>

### <span data-ttu-id="f28b5-135">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="f28b5-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="f28b5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f28b5-136">OUTPUTS</span></span>

### <span data-ttu-id="f28b5-137">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="f28b5-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="f28b5-138">Note</span><span class="sxs-lookup"><span data-stu-id="f28b5-138">NOTES</span></span>

<span data-ttu-id="f28b5-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f28b5-139">ALIASES</span></span>

<span data-ttu-id="f28b5-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f28b5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f28b5-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f28b5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f28b5-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f28b5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f28b5-143">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f28b5-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f28b5-144">`[EndpointName <String>]`: Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="f28b5-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="f28b5-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f28b5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f28b5-146">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f28b5-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f28b5-147">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f28b5-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f28b5-148">`[ResourceName <String>]`: Nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f28b5-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f28b5-149">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f28b5-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="f28b5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f28b5-150">RELATED LINKS</span></span>

