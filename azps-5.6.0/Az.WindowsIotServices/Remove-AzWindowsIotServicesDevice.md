---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: e0012bab0679a49e0ad5a117845ca9e0e5d5a6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971597"
---
# <span data-ttu-id="a63c4-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="a63c4-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="a63c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a63c4-103">Eliminare un servizio per dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a63c4-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a63c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a63c4-104">SYNTAX</span></span>

### <span data-ttu-id="a63c4-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a63c4-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a63c4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a63c4-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a63c4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a63c4-107">DESCRIPTION</span></span>
<span data-ttu-id="a63c4-108">Eliminare un servizio per dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a63c4-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a63c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a63c4-109">EXAMPLES</span></span>

### <span data-ttu-id="a63c4-110">Esempio 1: Rimuovere un servizio Windows IoT in base al nome</span><span class="sxs-lookup"><span data-stu-id="a63c4-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="a63c4-111">Questo comando rimuove un servizio Windows IoT in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a63c4-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="a63c4-112">Esempio 2: Rimuovere un servizio IoT di Windows tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="a63c4-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="a63c4-113">Questo comando rimuove un servizio IoT di Windows tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a63c4-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="a63c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63c4-114">PARAMETERS</span></span>

### <span data-ttu-id="a63c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63c4-115">-DefaultProfile</span></span>
<span data-ttu-id="a63c4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a63c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a63c4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a63c4-117">-InputObject</span></span>
<span data-ttu-id="a63c4-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a63c4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a63c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a63c4-119">-Name</span></span>
<span data-ttu-id="a63c4-120">Nome del servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a63c4-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a63c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a63c4-122">Nome del gruppo di risorse che contiene il servizio di dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="a63c4-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a63c4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a63c4-123">-SubscriptionId</span></span>
<span data-ttu-id="a63c4-124">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a63c4-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="a63c4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a63c4-125">-Confirm</span></span>
<span data-ttu-id="a63c4-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63c4-127">-WhatIf</span></span>
<span data-ttu-id="a63c4-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a63c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63c4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a63c4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63c4-130">CommonParameters</span></span>
<span data-ttu-id="a63c4-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63c4-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a63c4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63c4-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a63c4-133">INPUTS</span></span>

### <span data-ttu-id="a63c4-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a63c4-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="a63c4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a63c4-135">OUTPUTS</span></span>

### <span data-ttu-id="a63c4-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="a63c4-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="a63c4-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a63c4-137">NOTES</span></span>

<span data-ttu-id="a63c4-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a63c4-138">ALIASES</span></span>

<span data-ttu-id="a63c4-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a63c4-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a63c4-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a63c4-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a63c4-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a63c4-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a63c4-142">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a63c4-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a63c4-143">`[DeviceName <String>]`: nome del servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a63c4-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a63c4-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a63c4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a63c4-145">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il servizio dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="a63c4-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a63c4-146">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a63c4-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a63c4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a63c4-147">RELATED LINKS</span></span>

