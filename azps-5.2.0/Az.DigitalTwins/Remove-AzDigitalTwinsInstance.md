---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346972"
---
# <span data-ttu-id="a33f9-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a33f9-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="a33f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a33f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a33f9-103">Eliminare un DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a33f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a33f9-104">SYNTAX</span></span>

### <span data-ttu-id="a33f9-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a33f9-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a33f9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a33f9-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a33f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a33f9-107">DESCRIPTION</span></span>
<span data-ttu-id="a33f9-108">Eliminare un DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a33f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a33f9-109">EXAMPLES</span></span>

### <span data-ttu-id="a33f9-110">Esempio 1: rimuovere un AzDigitalTwinsInstance per nome</span><span class="sxs-lookup"><span data-stu-id="a33f9-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="a33f9-111">Questo comando rimuove un AzDigitalTwinsInstance per nome</span><span class="sxs-lookup"><span data-stu-id="a33f9-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="a33f9-112">Esempio 2: rimuovere un AzDigitalTwinsInstance da InputObject</span><span class="sxs-lookup"><span data-stu-id="a33f9-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="a33f9-113">Questo comando rimuove un AzDigitalTwinsInstance per nome</span><span class="sxs-lookup"><span data-stu-id="a33f9-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="a33f9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a33f9-114">PARAMETERS</span></span>

### <span data-ttu-id="a33f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a33f9-115">-AsJob</span></span>
<span data-ttu-id="a33f9-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a33f9-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33f9-117">-DefaultProfile</span></span>
<span data-ttu-id="a33f9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a33f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a33f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a33f9-119">-InputObject</span></span>
<span data-ttu-id="a33f9-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a33f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="a33f9-121">-NoWait</span></span>
<span data-ttu-id="a33f9-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a33f9-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a33f9-123">-PassThru</span></span>
<span data-ttu-id="a33f9-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a33f9-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="a33f9-126">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a33f9-127">-ResourceName</span></span>
<span data-ttu-id="a33f9-128">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a33f9-129">-SubscriptionId</span></span>
<span data-ttu-id="a33f9-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a33f9-130">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a33f9-131">-Confirm</span></span>
<span data-ttu-id="a33f9-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a33f9-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a33f9-133">-WhatIf</span></span>
<span data-ttu-id="a33f9-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a33f9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a33f9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a33f9-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33f9-136">CommonParameters</span></span>
<span data-ttu-id="a33f9-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a33f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33f9-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a33f9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33f9-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a33f9-139">INPUTS</span></span>

### <span data-ttu-id="a33f9-140">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="a33f9-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="a33f9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a33f9-141">OUTPUTS</span></span>

### <span data-ttu-id="a33f9-142">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a33f9-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a33f9-143">Note</span><span class="sxs-lookup"><span data-stu-id="a33f9-143">NOTES</span></span>

<span data-ttu-id="a33f9-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a33f9-144">ALIASES</span></span>

<span data-ttu-id="a33f9-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a33f9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a33f9-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a33f9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a33f9-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a33f9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a33f9-148">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a33f9-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a33f9-149">`[EndpointName <String>]`: Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="a33f9-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="a33f9-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a33f9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a33f9-151">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a33f9-152">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a33f9-153">`[ResourceName <String>]`: Nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="a33f9-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="a33f9-154">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a33f9-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a33f9-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a33f9-155">RELATED LINKS</span></span>

