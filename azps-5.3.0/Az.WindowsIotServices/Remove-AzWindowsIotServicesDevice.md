---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474692"
---
# <span data-ttu-id="3be2d-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="3be2d-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="3be2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3be2d-102">SYNOPSIS</span></span>
<span data-ttu-id="3be2d-103">Eliminare un servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="3be2d-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="3be2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3be2d-104">SYNTAX</span></span>

### <span data-ttu-id="3be2d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3be2d-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3be2d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3be2d-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3be2d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3be2d-107">DESCRIPTION</span></span>
<span data-ttu-id="3be2d-108">Eliminare un servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="3be2d-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="3be2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3be2d-109">EXAMPLES</span></span>

### <span data-ttu-id="3be2d-110">Esempio 1: rimuovere un servizio Windows un sacco di servizi per nome</span><span class="sxs-lookup"><span data-stu-id="3be2d-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="3be2d-111">Questo comando rimuove un servizio Windows un sacco di servizi per nome.</span><span class="sxs-lookup"><span data-stu-id="3be2d-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="3be2d-112">Esempio 2: rimuovere un servizio Windows un sacco di servizi per pipeline</span><span class="sxs-lookup"><span data-stu-id="3be2d-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="3be2d-113">Questo comando rimuove un servizio Windows molto per pipeline.</span><span class="sxs-lookup"><span data-stu-id="3be2d-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="3be2d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3be2d-114">PARAMETERS</span></span>

### <span data-ttu-id="3be2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be2d-115">-DefaultProfile</span></span>
<span data-ttu-id="3be2d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3be2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be2d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be2d-117">-InputObject</span></span>
<span data-ttu-id="3be2d-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3be2d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3be2d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3be2d-119">-Name</span></span>
<span data-ttu-id="3be2d-120">Nome del servizio di dispositivo Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="3be2d-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="3be2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="3be2d-122">Il nome del gruppo di risorse che contiene il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="3be2d-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="3be2d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3be2d-123">-SubscriptionId</span></span>
<span data-ttu-id="3be2d-124">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3be2d-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="3be2d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3be2d-125">-Confirm</span></span>
<span data-ttu-id="3be2d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3be2d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be2d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be2d-127">-WhatIf</span></span>
<span data-ttu-id="3be2d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3be2d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be2d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3be2d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be2d-130">CommonParameters</span></span>
<span data-ttu-id="3be2d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be2d-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3be2d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be2d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3be2d-133">INPUTS</span></span>

### <span data-ttu-id="3be2d-134">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="3be2d-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="3be2d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3be2d-135">OUTPUTS</span></span>

### <span data-ttu-id="3be2d-136">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="3be2d-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="3be2d-137">Note</span><span class="sxs-lookup"><span data-stu-id="3be2d-137">NOTES</span></span>

<span data-ttu-id="3be2d-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3be2d-138">ALIASES</span></span>

<span data-ttu-id="3be2d-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3be2d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3be2d-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3be2d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3be2d-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3be2d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3be2d-142">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3be2d-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3be2d-143">`[DeviceName <String>]`: Nome del servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="3be2d-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="3be2d-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3be2d-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3be2d-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene il servizio dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="3be2d-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="3be2d-146">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3be2d-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="3be2d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3be2d-147">RELATED LINKS</span></span>

